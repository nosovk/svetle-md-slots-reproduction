<script context="module">
  import { h1, h2, blockquote } from './components.js';
  export { h1, h2, blockquote };
</script>
<script lang="ts">
  export let title;
</script>

<svelte:head>
  <title>{title}</title>
</svelte:head>

<h1 class="page-title">{title}</h1>
<div class="container faq">
  <slot />
</div>
