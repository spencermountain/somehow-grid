<script>
  import { onMount } from 'svelte'
  import { parts } from './store.js'
  export let height = 800
  export let width = 400
  export let total = 100
  onMount(() => {
    console.log($parts)
  })
</script>

<style>
  .box {
    border-radius: 0px;
    margin-top: 2px;
    min-width: 6px;
    min-height: 6px;
    border-left: 1px solid white;
  }
</style>

<div>grid</div>
<slot />
