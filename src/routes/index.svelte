<script>
  import Hello from '../components/Hello.svelte'
</script>
<style>
  .home-container {
    align-items: center;
    display: flex;
    flex: 1;
    justify-content: center;
    margin: 2em 0;
    min-height: 400px;
  }

  .home-copy {
    flex: 1;
  }
  
  p {
    font-size: 1.4em;
    line-height: 1.5;
  }

  img {
    width: 100%;
    max-width: 400px;
  }

  @media (max-width: 1020px) {
    p {
      font-size: 1.2em;
    }

    img {
      max-width: 300px;
    }
  }

  @media (max-width: 800px) {
    .home-container {
      flex-direction: column;
      color: #D9DAF8;
    background-color: #48485F;
    }

    .home-copy {
      flex: 0;
      padding-bottom: 2em;
      text-align: center;
    }
  }
</style>

<svelte:head>
  <title>jacob stordahl</title>
</svelte:head>

<div class="home-container">
  <figure>
    <img src="memoji.png" alt="">
  </figure>
  <div class="home-copy">
    <Hello />
    <p>my name is jacob stordahl and I’m a jr. developer living and working in the beautiful PNW. I’ve been writing html & css for years; however I recently decided to leave my career as a fabricator to pursue development full-time. i’m currently working towards becoming a full-stack javascript developer. make sure to follow me on twitter to see what I’m up to!</p>
  </div>
</div>
