<script>
  import AdminCardSection1 from '../components/sections/AdminCardSection1.svelte'
  import BreadcrumbSection from '../components/sections/BreadcrumbSection.svelte'
  import ChartSection1 from '../components/sections/ChartSection1.svelte'
  import TableSection from '../components/sections/TableSection.svelte'
  import MDBContainer from 'mdbsvelte/src/MDBContainer.svelte'
</script>
<MDBContainer fluid>
  <BreadcrumbSection />
  <AdminCardSection1 />
  <ChartSection1 />
  <TableSection />
</MDBContainer>
