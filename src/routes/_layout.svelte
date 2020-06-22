<script>
  import Header from '../components/Header.svelte';

  export let segment;
</script>

<style>
  .layout {
    display: flex;
    flex-direction: column;
    min-height: 100%;
    min-height: 100vh;
  }

  main {
    flex: 1;
    position: relative;
    margin: 0 auto;
    max-width: 1400px;
    /* background-color: white; */
    padding: 1em 2em;
    box-sizing: border-box;
    width: 100%;
    display: flex;
    flex-direction: column;
  }
  i{
    font-size:1.5rem;
    margin-bottom:1rem;
  }

  footer {
    font-size: 1em;
    font-family: 'Anonymous Pro', monospace;
    margin: 1em auto;
    max-width: 1400px;
    padding: 1em 2em;
    text-align: center;
    width: 100%;
  }
</style>

<div class="layout">
  <Header {segment}/>

  <main>
    <slot></slot>
  </main>

  <footer>
    <div>
      <a href="https://github.com/stordahl"><i class="fa fa-github" aria-hidden="true"></i></a>
      <a href="https://twitter.com/queeryselector"><i class="fa fa-twitter" aria-hidden="true"></i></a>
      <a href="https://instagram.com/queeryselector"><i class="fa fa-instagram" aria-hidden="true"></i></a>
    </div>
    <span>
      &copy; {new Date().getFullYear()} Jacob Stordahl.
      Powered by <a href="https://sapper.svelte.dev" target="_blank">Sapper</a>.
    </span>
  </footer>
</div>
