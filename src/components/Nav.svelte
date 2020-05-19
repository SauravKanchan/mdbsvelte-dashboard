<script>
  export let segment;
  export let isOpen;
  import {fly} from 'svelte/transition';
  import MDBNavLink from 'mdbsvelte/src/MDBNavLink.svelte';


</script>

<style>
  .sidebar {
    min-width: 250px;
    max-width: 250px;
    min-height: 100vh;
    z-index: 100;
    position: fixed;
  }
</style>
{#if isOpen}
  <nav class="sidebar bg-dark  p-5" transition:fly="{{ x:-250, y: 0, duration: 500 }}">
    <MDBNavLink class="text-white" active href="/">Home</MDBNavLink>
    <MDBNavLink class="text-white" href="/about">About</MDBNavLink>
    <MDBNavLink class="text-white" href="/blog">Blog</MDBNavLink>
  </nav>
{/if}
