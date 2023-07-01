<script lang="ts">
  import plzDemoLogo from '/plz-demo-logo.svg'
  import DropdownDemo from './lib/DropdownDemo.svelte'
</script>

<main>
  <div>
    <img src={plzDemoLogo} class="logo" alt="PLZ Demo Logo" />
  </div>
  <h1>PLZ Dropdown Demo</h1>

  <div class="card">
    <DropdownDemo />
  </div>

  <p>
    Check out <a href="https://github.com/3n3a/plz-api" target="_blank" rel="noreferrer">Source Code for the API</a>, or the <a href="https://github.com/3n3a/plz-dropdown" target="_blank" rel="noreferrer">Source Code for the Dropdown Demo</a>!
  </p>

  <p class="read-the-docs">
    This dropdown and the API only display postal codes for the region of Switzerland.
  </p>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style>
