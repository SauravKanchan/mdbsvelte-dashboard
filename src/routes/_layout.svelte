<script>
  import SideNavigation from "../components/SideNavigation.svelte";
  import TopNavigation from "../components/TopNavigation.svelte";

  let isOpen = true;
  export let segment;
</script>

<style>
  .active {
    margin-left: 250px;
  }
  .content {
    width: 100%;
    transition: 0.5s margin cubic-bezier(0.22, 1, 0.36, 1);
  }
</style>

<div class="flexible-content">
  <TopNavigation />
  <SideNavigation {segment} {isOpen} />
  <slot />
</div>
