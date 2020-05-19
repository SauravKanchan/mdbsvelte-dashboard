<script>
  import Nav from "../components/Nav.svelte";

  import MDBRow from "mdbsvelte/src/MDBRow.svelte";
  import MDBNavbar from "mdbsvelte/src/MDBNavbar.svelte";
  import MDBNavbarBrand from "mdbsvelte/src/MDBNavbarBrand.svelte";
  import MDBIcon from "mdbsvelte/src/MDBIcon.svelte";
  import MDBBtn from "mdbsvelte/src/MDBBtn.svelte";
  import MDBNavbarNav from "mdbsvelte/src/MDBNavbarNav.svelte";

  import { fly } from "svelte/transition";
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

<MDBRow class="wrapper">
  <Nav {segment} {isOpen} />
  <div class="content" class:active={isOpen}>
    <MDBNavbar color="primary-color" dark expand="md">
      <MDBBtn color="light-blue" on:click={() => (isOpen = !isOpen)}>
        <MDBIcon fas icon="align-justify" />
      </MDBBtn>
      <MDBNavbarNav right>
        <MDBNavbarBrand>
          <strong class="white-text">Admin</strong>
        </MDBNavbarBrand>
      </MDBNavbarNav>
    </MDBNavbar>
    <slot />
  </div>
</MDBRow>
