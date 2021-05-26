<script lang="ts">
  import '../app.scss';
</script>


<main>
  <slot />
</main>


<style lang="scss">
  main {
    flex: 1;
    display: flex;
    position: relative;
    flex-direction: column;
    padding: 1.25rem;
    width: 100%;
    margin: 0 auto;
  }
</style>
