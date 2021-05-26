---
layout: faq
title: faq
---

<script>
   // todo: next line added to show how it intended to work, with direct component invocation from md
    import Blockquote from '$lib/Faq/blockquote.svelte';
</script>

# Big Header1!


> ## block title?
> content block.  [more info](https://duckduckgo.com "block title")

> ## another block title?
> block content wit big amount of text
> like lorem ipsum etc
> with links etc. [more info](https://duckduckgo.com "another block title")

<Blockquote 
    question={'block title?'}>
content block
</Blockquote>

<Blockquote 
    question={'another block title?'}>
block content wit big amount of text like lorem ipsum etc with links etc.
</Blockquote>

# Another block of questions

<Blockquote 
    question={'block title?'}>
content block
</Blockquote>

<Blockquote 
    question={'block title?'}>
content block
</Blockquote>
