<script>
	import { fade, fly } from "svelte/transition";
  import "../app.css";
	import Tab1 from "./Tab1.svelte";
	import Tab2 from "./Tab2.svelte";
	import Tab3 from "./Tab3.svelte";
	import { backOut } from "svelte/easing";

  let tab = 1;

  const handleClick = (x) => {
    tab = x
  };


</script>


<div class="wrapper">
  <section class="contain">

    <nav>
      <div class="tabs">
        <a class="{tab==0 ? "tab tab-lifted tab-active" : "tab tab-lifted mobile"}" ></a> 
        <a class="{tab==0 ? "tab tab-lifted tab-active" : "tab tab-lifted"}" ></a> 
        <a class="{tab==1 ? "tab tab-lifted tab-active" : "tab tab-lifted"}"  on:click={() => handleClick(1)}>Intro</a> 
        <a class="{tab==2 ? "tab tab-lifted tab-active" : "tab tab-lifted"}" on:click={() => handleClick(2)}>Skills</a> 
        <a class="{tab==3 ? "tab tab-lifted tab-active" : "tab tab-lifted"}" on:click={()=>handleClick(3)}>Projects</a>
        <a class="{tab==4 ? "tab tab-lifted tab-active" : "tab tab-lifted"}" ></a>
        <a class="{tab==4 ? "tab tab-lifted tab-active" : "tab tab-lifted mobile"}" ></a>
      </div>
    </nav>

    {#if tab==1}
      <div in:fly={{ x: -100 }} out:fly={{ x: -100 }}>
        <Tab1 />
      </div>
    {/if}

    {#if tab==2}
    <div in:fly={{ x: 100 }} out:fly={{ x: -100 }}>
      <Tab2 />
    </div>
    {/if}

    {#if tab==3}
    <div in:fly={{ x: 100, delay:300 }} out:fly={{ x: -100 }}>
      <Tab3 />
    </div>
    {/if}

    <footer>
      <p>Made by Lukman Abdulkarim © 2023</p>
    </footer>
  </section>
</div>

<style>

  div {
    width: 100%;
  }

  p {
    color: rgba(255, 255, 255, 0.5);
  }

  a {
    background-color: #000;
  }

  .mobile {
    display: none;
  }
  .wrapper {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items:center;
  }

  .contain {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items:center;
  color: white;
  width: 100%;
  max-width: 800px;
  padding: 0 2.5em 2.5em 2.5em;
  }

  nav {
    margin: 2em 0;
    display: flex;
    flex-direction: row;
    justify-content: center;
  }


  .tab {
    color: rgb(255, 255, 255);

  }

  .tab-lifted {
    background-color: black;
  }

  .tab-active {
    color: black;

  }

  @media (min-width: 800px) {

    .mobile {
      display: block;
    }
  }

</style>