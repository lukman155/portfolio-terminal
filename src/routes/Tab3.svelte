<script>
	import { onMount } from "svelte";

  const projects = [
    { 
      name:'FMRepEX',
      desc:'FMRepEx (Facility Management Representative Expert) is a software solution that helps organizations manage their facilities and assets more efficiently and effectively. It can be used to track and manage work orders, preventive maintenance, inventory, and other facility-related tasks.',
      alt: 'icon',
      tech:['Svelte', 'JavaScript', 'Firebase', 'TailwindCSS', 'Vercel'],
      image:"/fmrep.png",
      liveUrl:'https://fmrep-frontend.vercel.app/',
      sourceCode:'https://github.com/lukman155/fmrep-frontend',
      color: 'rgba(255, 255, 255, 0.15)',
    },
    { 
      name:'Studio Umami',
      desc:'I crafted a bespoke digital experience for Studio Umami, leveraging cutting-edge technologies to enhance their online presence. I worked closely with them to understand their unique needs and develop a website that would meet those needs. I then utilized best practices to create a website that is fast, secure, and user-friendly.',
      alt: 'icon',
      tech:['Svelte', 'JavaScript', 'TailwindCSS', 'Vercel'],
      image:"/studio-umami.png",
      liveUrl:'https://studio-umami-agency.vercel.app/',
      sourceCode:'https://github.com/lukman155/studio-umami-agency',
      color: 'rgba(255, 255, 255, 0.15)',
    },
    { 
      name:'Landlrd',
      desc:'"Landlrd", a student accommodation rental application meticulously crafted with Ruby on Rails and Bootstrap. It sharpened my proficiency in problem-solving, robust database management, intricate user authentication, and responsive design.',
      alt: 'icon',
      tech:['Ruby on Rails', 'JavaScript', 'Bootstrap', 'Render', 'PostgreSQL'],
      image:"/landlrd.png",
      liveUrl:'https://landlrd.onrender.com/',
      sourceCode:'https://github.com/lukman155/landlord',
      color: 'rgba(0, 128, 0, 0.15)',
    },
    { 
      name:'GetLinked',
      desc:'Precision and pixel-perfection took the forefront for this project. I meticulously translated design concepts into code, ensuring every element, layout, and detail matched the original vision flawlessly. This project highlights my commitment to design fidelity and attention to detail.',
      alt: 'icon',
      tech:['Svelte', 'JavaScript', 'TailwindCSS', 'Vercel'],
      image:"/getlinked.png",
      liveUrl:'https://getlinked-pink.vercel.app/',
      sourceCode:'https://github.com/lukman155/getlinked',
      color: 'rgba(128, 0, 128, 0.15)',
    },
    { 
      name:'Magic Maths',
      desc:'Applied techniques learned from Practical React - writing requirements, iterating, and structuring app as an MVC. This really helped me build a much better foundation in React and JavaScript for web development. No frameworks were used. Design is based off the original Apple Iphone Calculator.',
      alt: 'icon',
      tech:['React', 'JavaScript', 'Render'],
      image:"/magicmaths.png",
      liveUrl:'https://math-magic-react-static.onrender.com/',
      sourceCode:'https://github.com/lukman155/magicmaths',
      color: 'rgba(255,255,153, .15)',
    },
    { 
      name:'PlayFree',
      desc:'PlayFree is a React web application that fetches data from a catalogue of free-to-play games and displays it in a user-friendly way. It allowed me to learn and practice, fetching data from remote APIs, rendering data in React components, styling React components, and deploying React applications.',
      alt: 'icon',
      tech:['React', 'JavaScript', 'Vercel'],
      image:"/playfree.png",
      liveUrl:'https://playfree.vercel.app/',
      sourceCode:'https://github.com/lukman155/playfree',
      color: 'rgba(0,74,74,.15)',
    },
  ];

  onMount(()=>{
    const cards = document.querySelectorAll('.color');
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
      <a href={project.sourceCode} class="btn btn-xs sm:btn-sm btn-primary source-btn">Source Code</a>
      <a href={project.liveUrl} target="_blank" class="btn btn-xs sm:btn-sm btn-primary live-btn">Live Link <span>&#8594;</span></a>
    </div>
  </div>
</div>
{/each}

<style>

.color {
  transition: background-color 0.3s ease; /* Add a transition effect for smoother color change */
}


.source-btn {
  margin-left: 2px;
}

.source-btn:hover, .live-btn:hover {
  background-color: rgb(37, 37, 37);
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
    font-size: 1.6em;
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
  height: 320px;
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