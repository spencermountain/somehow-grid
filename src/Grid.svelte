<script>
  import { onMount } from 'svelte'
  import { parts } from './store.js'
  export let total = 100
  let squares = []
  const calculate = function(parts) {}
  onMount(() => {
    squares = []
    $parts.forEach(o => {
      let num = Number(o.count)
      for (let i = 0; i < num; i += 1) {
        squares.push(o.color)
      }
    })
    // add the rest
    for (let i = squares.length; i < total; i += 1) {
      squares.push('#fafaf0')
    }
  })
</script>

<style>
  .container {
    position: relative;
    border-bottom: 4px solid lightsteelblue;
    padding-top: 0.4rem;
    padding-bottom: 0.4rem;
    padding-left: 0.2rem;
    padding-right: 0.2rem;
    line-height: 1rem;
    box-shadow: 1px 2px 8px 0px rgba(0, 0, 0, 0.2);
  }
  .row {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
    text-align: center;
    flex-wrap: wrap;
    align-self: stretch;
  }
  .box {
    margin: 1px;
    width: 10px;
    min-height: 10px;
  }
</style>

<div class="container row" style="width:100%;">
  {#each squares as c}
    <div class="box" style="background-color:{c};" />
  {/each}
</div>
<slot />
