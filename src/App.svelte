<script>
  import Header from "./components/Header.svelte";
</script>

<style type="text/scss">
  $color: red;

  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<Header />
<main>
  <h1>Hello from App.svelte</h1>
</main>
