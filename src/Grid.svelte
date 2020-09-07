<script>
  import { onMount } from 'svelte'
  import { parts } from './store.js'
  export let total = 100
  export let size = 10
  let squares = []
  let labels = []

  const percent = function(already, val, total) {
    let height = (val / total) * 100
    let top = (already / total) * 100
    return top + height / 3
  }

  const calculate = function(parts) {
    squares = []
    labels = []
    let already = 0
    parts.forEach(o => {
      let num = Number(o.count)
      if (o.label) {
        labels.push({
          label: o.label,
          color: o.color,
          top: percent(already, num, total),
        })
      }
      already += num
      for (let i = 0; i < num; i += 1) {
        squares.push(o.color)
      }
    })
    // add the rest
    for (let i = squares.length; i < total; i += 1) {
      squares.push('#fafaf0')
    }
  }

  onMount(() => {
    calculate($parts)
  })
</script>

<style>
  .labels {
    position: relative;
    min-width: 50px;
    padding: 0.75rem;
    text-align: left;
  }
  .label {
    position: absolute;
    width: 50px;
    padding-top: 1rem;
    padding-bottom: 1rem;
  }
  .container {
    display: flex;
    flex-wrap: nowrap;
  }
  .squares {
    padding-top: 0.4rem;
    padding-bottom: 0.4rem;
    padding-left: 0.2rem;
    padding-right: 0.2rem;
    box-shadow: 1px 2px 8px 0px rgba(0, 0, 0, 0.2);
    border-bottom: 4px solid lightsteelblue;
    position: relative;
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
  }
</style>

<div class="container" style="width:100%;">
  <div class="labels">
    {#each labels as l}
      <div class="label" style="color:{l.color}; border-right:3px solid {l.color}; top:{l.top}%;">{l.label}</div>
    {/each}
  </div>
  <div class="squares">
    {#each squares as c}
      <div class="box" style="background-color:{c}; width:{size}px; height:{size}px;" />
    {/each}
  </div>
</div>
<slot />
