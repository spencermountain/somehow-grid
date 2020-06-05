<script>
  import c from 'spencer-color'
  import { parts } from './store.js'
  export let color = 'steelblue'
  export let count = 10
  let colors = c.colors
  parts.update(arr => {
    arr.push({
      color: colors[color] || color,
      count: count,
    })
    return arr
  })
</script>

<style>

</style>

<div />
