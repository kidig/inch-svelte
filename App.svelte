<script>
  import Converter from "./Converter.svelte";
</script>

<main>
  <div class="converter">
    <h1>inch to cm</h1>
    <Converter />
  </div>
  <div class="footer">2023 &copy; kidig</div>
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
    height: 100%;
    width: 100%;
  }

  :global(body) {
    height: 100%;
    width: 100%;
    margin: 0 auto;
  }

  main {
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 20px;
  }

  h1 {
    text-align: center;
    padding-top: 20px;
  }

  .converter {
    flex: 1;
  }

  .footer {
    flex: 1;
    display: flex;
    align-items: flex-end;
    padding: 10px 0;
    font-size: 0.8em;
  }
</style>
