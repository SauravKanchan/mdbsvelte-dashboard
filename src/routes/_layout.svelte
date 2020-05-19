<script>
  import Nav from '../components/Nav.svelte';

  import MDBRow from 'mdbsvelte/src/MDBRow.svelte';
  import MDBNavbar from 'mdbsvelte/src/MDBNavbar.svelte'
  import MDBNavbarBrand from 'mdbsvelte/src/MDBNavbarBrand.svelte'
  import MDBBtn from 'mdbsvelte/src/MDBBtn.svelte'
  import MDBNavbarNav from 'mdbsvelte/src/MDBNavbarNav.svelte'


  let isOpen = true;
  export let segment;
</script>
<style>
  .active{
    margin-left: 250px
  }
</style>

<MDBRow class="wrapper">
  <Nav {segment} {isOpen}/>
  <div style="width: 100%" class:active={isOpen}>
    <MDBNavbar color="primary-color" dark expand="md">
      <MDBBtn color="light-blue" on:click={ ()=>isOpen = !isOpen}/>
      <MDBNavbarNav right>
        <MDBNavbarBrand>
          <strong class="white-text">Admin</strong>
        </MDBNavbarBrand>
      </MDBNavbarNav>
    </MDBNavbar>
    <slot></slot>
  </div>
</MDBRow>
