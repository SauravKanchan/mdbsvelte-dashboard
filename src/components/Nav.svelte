<script>
  export let segment;
  export let isOpen;
  import { fly } from "svelte/transition";
  import { quintOut } from "eases-jsnext";
  import MDBNavLink from "mdbsvelte/src/MDBNavLink.svelte";
</script>

<style>
  .sidebar {
    z-index: 100;
    position: fixed;
    min-width: 250px;
    max-width: 250px;
    min-height: 100vh;
    left: -250px;
    transition: 0.5s all cubic-bezier(0.22, 1, 0.36, 1);
  }
  .sidebar-open {
    left: 0;
  }
</style>

<nav class="sidebar bg-dark p-5" class:sidebar-open={isOpen}>
  {#if isOpen}
    <MDBNavLink class="text-white" active href="/">Home</MDBNavLink>
    <MDBNavLink class="text-white" href="/about">About</MDBNavLink>
    <MDBNavLink class="text-white" href="/blog">Blog</MDBNavLink>
  {/if}

</nav>
