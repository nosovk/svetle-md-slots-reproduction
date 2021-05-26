<script>
  import { setContext, getContext } from 'svelte';
  import dropcap from '$lib/Faq/dropcap.svg';
  const level = getContext('level') || 0;
  setContext('level', level + 1);
  
</script>

<div class="paragraph row">
  <div class="icon-wrapper">
    <img src={dropcap} alt="logo" />
  </div>
  <h1><slot /></h1>
</div>

<style lang="scss">
  .paragraph {
    .icon-wrapper {
      padding: 1rem;

      img {
        width: 2.81rem;
        height: auto;
      }
    }

    h1 {
      @include font(var(--size-14), var(--weight-500), var(--color-header-light));
    }
  }
</style>
