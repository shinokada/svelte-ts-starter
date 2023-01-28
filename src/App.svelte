<script lang="ts">
  import Router, { link } from "svelte-spa-router";
  import { routes } from "./routes.js";
  import { onMount } from "svelte";
  import { Alert } from "flowbite-svelte";
  let data;
  async function fetchData() {
    const response = await fetch(import.meta.env.VITE_API_ENDPOINT);
    data = await response.json();
  }
  onMount(fetchData);
</script>

<main class="p-4">
  <Router {routes} />

  {#if data}
    <p>Data:</p>
    <ul>
      {#each Object.entries(data) as [key, value]}
        <li>{key}: {value}</li>
      {/each}
    </ul>
  {/if}
</main>
