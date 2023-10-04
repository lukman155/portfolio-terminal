
<div class="card card-side glass">
  <figure>
    <img src="/studio-umami.png" alt="car!" class="hover-image" />
  </figure>
  <div class="card-body">
    <h2 class="card-title">Studio Umami</h2>
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus quos commodi non nulla, dolore consequatur facere tempora atque error dolor est sequi odit eveniet, voluptatem quisquam porro vero culpa voluptas..</p>
    <div class="badges">
      <span class="badge badge-outline">Svelte</span>
      <span class="badge badge-outline">JavaScript</span>
      <span class="badge badge-outline">TailWindCSS</span>
      <span class="badge badge-outline">Badge</span>
    </div>
    <div class="card-actions justify-stretch">
      <button class="btn btn-sm btn-primary">Live Link</button>
      <button class="btn btn-sm btn-primary">Source Code</button>
    </div>
  </div>
</div>




<style>
  .badges {
    margin-bottom: 1em;

  }
  span {
    font-size: .5em;
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