<div class="intro slide-enter-content">
  <h1> <span class="float">></span> Lukman Abdulkarim<span class="blinking-cursor">|</span></h1>
  <p>Hey, I am Lukman Abdulkarim, a battle-hardened full-stack web developer.</p>
  <br>
  <p>Building simple, beautiful and interactive user experiences is where my passion lies. You can find my full projects list here.</p>
  <br>
  <p>Interactivity is the lifeblood of a website. It's what keeps visitors engaged and coming back for more.</p>
  <br>
  <p>Outside of programming, I enjoy playing chess and practicing Judo. If you happen to be in the same city I live, maybe we can hang out and code together.</p>
</div>

<h2>Connect with me on</h2>
<div class="socials slide-left-content">
  
  <a href="/" class="links"><i class="fa-brands fa-github"></i> Github</a>
  <a href="/" class="links"><i class="fa-brands fa-linkedin-in"></i> LinkedIn</a>
  <a href="/" class="links"><i class="fa-brands fa-x-twitter"></i> X (Twitter)</a>
  <a href="/" class="links"><i class="fa-brands fa-instagram"></i> Instagram</a>
  <a href="/" class="links"><i class="fa-brands fa-angellist"></i> AngelList</a>
  <a href="/" class="links"><i class="fa-brands fa-youtube"></i> Youtube</a>
</div>

<style>

  .socials {
    font-size: .8em;
    display: flex;
    gap: 1em;
    flex-wrap: wrap;
    color: #ffffff7d;
  }

  a {
    text-decoration: underline;
    text-decoration-color: #ffffff25;
    text-underline-offset: 5px;
    transition: all 0.3s ease-out;
  }

  a:hover {
    text-underline-offset: 10px;
    text-decoration-color: #ffffff;
  }

  .float {
    position: absolute;
    left: -1em;
    color: #ffffff25;
  }

  .intro {
    margin: 0 0 5em 0;
  }
  
  h1 {
    font-size: 2em;
    font-weight: 700;
    margin: 1em 0;
  }

  h2 {
    align-self: flex-start;
    font-weight: 600;
    color: #ffffffe1;
    margin: 0 0 1em 0;
  }

  p {
    color: #ffffffa4;
  }


  .blinking-cursor {
    color: #ffffff;
    animation: 1s blink step-end infinite;
  }

@keyframes blink {
  from, to {
    color: inherit;
  }
  50% {
    color: black;
  }
}

@keyframes slide-enter {
  0% {
    transform: translateY(10px);
    opacity: 0
  }

  to {
    transform: translateY(0);
    opacity: 100
  }
}

@keyframes slide-left {
  0% {
    transform: translateX(-10px);
    opacity: 0
  }

  to {
    transform: translatex(0);
    opacity: 100
  }
}

.slide-left-content > * {
  --stagger: 0;
  --delay: 150ms;
  --start: 0ms;
  animation: slide-left 1s both 1;
  animation-delay: calc(var(--start) + var(--stagger) * var(--delay));
}

.slide-left-content > *:nth-child(1) { --stagger: 8; }
.slide-left-content > *:nth-child(2) { --stagger: 9; }
.slide-left-content > *:nth-child(3) { --stagger: 10; }
.slide-left-content > *:nth-child(4) { --stagger: 11; }
.slide-left-content > *:nth-child(5) { --stagger: 12; }
.slide-left-content > *:nth-child(6) { --stagger: 13; }

.slide-enter-content > * {
  --stagger: 0;
  --delay: 150ms;
  --start: 0ms;
  animation: slide-enter 1s both 1;
  animation-delay: calc(var(--start) + var(--stagger) * var(--delay));
}

.slide-enter-content > *:nth-child(2) { --stagger: 0; }
.slide-enter-content > *:nth-child(3) { --stagger: 1; }
.slide-enter-content > *:nth-child(4) { --stagger: 2; }
.slide-enter-content > *:nth-child(5) { --stagger: 3; }
.slide-enter-content > *:nth-child(6) { --stagger: 4; }
.slide-enter-content > *:nth-child(6) { --stagger: 5; }
.slide-enter-content > *:nth-child(7) { --stagger: 6; }
.slide-enter-content > *:nth-child(8) { --stagger: 7; }


@media (min-width: 800px) {

  h1 {
    font-size: 3em;
    font-weight: 700;
    margin: 1.5em 0;
  }

.mobile {
  display: block;
}
}
</style>