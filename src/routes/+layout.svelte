<script lang="ts">
  import { base } from "$app/paths";
</script>

<div class="app">
  <header>
    <h1><a href="{base}/" class="logo">🍞 Hovis' McGrobo;sBag of Bread</a></h1>
    <!-- <nav></nav> -->
  </header>

  <main>
    <slot />
  </main>

  <footer>
    <div>
      <pre>Crumbs and nuggets for the Hovis-inclined</pre>
    </div>
  </footer>
</div>

<style>
  :global(body) {
    margin: 0;
    padding: 0;
    font-family:
      system-ui,
      -apple-system,
      BlinkMacSystemFont,
      "Segoe UI",
      Roboto,
      "Helvetica Neue",
      Arial,
      sans-serif;
    background: linear-gradient(135deg, #f5deb3 0%, #f4a460 100%);
    min-height: 100vh;
  }

  :global(*) {
    box-sizing: border-box;
  }

  .app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  header {
    background: linear-gradient(90deg, #d2691e 0%, #8b4513 100%);
    padding: 1rem 2rem;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  /*nav {
    max-width: 1200px;
    margin: 0 auto;
  }*/

  .logo {
    font-size: 2rem;
    font-weight: bold;
    color: #fff8dc;
    text-decoration: none;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
    transition: transform 0.2s;
    display: inline-block;
  }

  .logo:hover {
    transform: scale(1.05) rotate(-2deg);
  }

  main {
    flex: 1;
    padding: 2rem;
    max-width: 1200px;
    margin: 0 auto;
    width: 100%;
  }

  footer {
    background: linear-gradient(90deg, #8b4513 0%, #654321 100%);
    color: #fff8dc;
    text-align: center;
    padding: 1.5rem;
    margin-top: 2rem;
    font-style: italic;
  }

  footer pre {
    margin: 0;
  }
</style>
