<!-- routify:options preload="proximity" -->
<script>
  import Nav from '../components/Nav/Nav.svelte'
  import Footer from '../components/Footer/Footer.svelte'
</script>
<style>
  .content{
    min-height: calc(100vh - 150px);
  }
</style>
<Nav />
<div class="content">
  <slot />
</div>
<Footer />