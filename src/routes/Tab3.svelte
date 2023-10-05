<script>
	import { onMount } from "svelte";

  const projects = [
    { 
      name:'Studio Umami',
      desc:'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus quos commodi non nulla, dolore consequatur facere tempora atque error dolor est sequi odit eveniet, voluptatem quisquam porro vero culpa voluptas..',
      alt: 'icon',
      tech:['Svelte', 'JavaScript', 'TailwindCSS', 'Vercel'],
      image:"/studio-umami.png",
      liveUrl:'/',
      sourceCode:'/',
      color: 'rgba(255, 255, 255, 0.1)',
    },
    { 
      name:'Landlrd',
      desc:'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus quos commodi non nulla, dolore consequatur facere tempora atque error dolor est sequi odit eveniet, voluptatem quisquam porro vero culpa voluptas..',
      alt: 'icon',
      tech:['Ruby on Rails', 'JavaScript', 'Bootstrap', 'Render', 'PostgreSQL'],
      image:"/studio-umami.png",
      liveUrl:'/',
      sourceCode:'/',
      color: 'rgba(0, 128, 0, 0.1)',
    },
    { 
      name:'GetLinked',
      desc:'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus quos commodi non nulla, dolore consequatur facere tempora atque error dolor est sequi odit eveniet, voluptatem quisquam porro vero culpa voluptas..',
      alt: 'icon',
      tech:['Svelte', 'JavaScript', 'TailwindCSS', 'Vercel'],
      image:"/studio-umami.png",
      liveUrl:'/',
      sourceCode:'/',
      color: 'rgba(128, 0, 128, 0.1)',
    },
    { 
      name:'Studio Umami',
      desc:'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus quos commodi non nulla, dolore consequatur facere tempora atque error dolor est sequi odit eveniet, voluptatem quisquam porro vero culpa voluptas..',
      alt: 'icon',
      tech:['Svelte', 'JavaScript', 'TailwindCSS', 'Vercel'],
      image:"/studio-umami.png",
      liveUrl:'/',
      sourceCode:'/',
      color: 'rgba(255, 255, 255, 0.1)',
    },
  ];

  onMount(()=>{
      const cards = document.querySelectorAll('.color');
    console.log(cards);
    cards.forEach((card) => {
      card.addEventListener('mouseenter', () => {
        const index = card.getAttribute('data-index');
        const hoverColor = projects[index].color;
        card.style.setProperty('--hover-color', hoverColor);
      });

      card.addEventListener('mouseleave', () => {
        card.style.removeProperty('--hover-color');
      });
    });
  })
  


</script>

{#each projects as project, i}
<div class="card card-side glass color" key={i} data-index={i}>
  <figure>
    <img src={project.image} alt class="hover-image" />
  </figure>
  <div class="card-body">
    <h2 class="card-title">{project.name}</h2>
    <p>{project.desc}</p>
    <div class="badges">
      {#each project.tech as technology}
      <span class="badge badge-outline">{technology}</span>
      {/each}
    </div>
    <div class="card-actions justify-stretch">
      <a href={project.liveUrl} class="btn btn-sm btn-primary">Live Link</a>
      <a href={project.sourceCode} class="btn btn-sm btn-primary">Source Code</a>
    </div>
  </div>
</div>
{/each}

<style>

.color {
  transition: background-color 0.3s ease; /* Add a transition effect for smoother color change */
}

.color:hover {
  background-color: var(--hover-color); /* Use a CSS variable for the background color on hover */
}

  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: .4em;
    margin-bottom: 1em;

  }
  span {
    font-size: .7em;  
  }

  h2 {
    font-size: 1.8em;
    margin-bottom: 1em;
  }

  p {
    font-size: .8em;
    font-weight: 100;
  }



  .card {
  position: relative;
  flex-direction: column;
  margin-bottom: 3em;
}


  .card-body {
    max-width: 500px;
  }

  button {
    font-size: .7em;
  }

  .hover-image {
    display: none;
  }

.card:hover .hover-image {
  opacity: 1; /* Make the image fully visible */
}

  .btn {
    background:rgb(71, 71, 71);
    border: black;
  }

  
  @media (min-width:800px){
    .card {
  flex-direction: row;
}

    .hover-image {
      display: block;
      width: 300px;
      height: 100%;
      object-fit: cover;
      transition: all .3s ease-in-out;
    }

  }

</style>