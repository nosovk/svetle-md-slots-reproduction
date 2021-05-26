<script context="module" lang="ts">
  export const prerender = true;
</script>

<svelte:head>
  <title>main</title>
</svelte:head>


  <section>
    <div class="container">
      <a href="faq">troublesome page</a>
    </div>
  </section>

<style lang="scss">
  section {
    flex: 1;
    .container {
      @extend %container;
    }
  }
</style>
