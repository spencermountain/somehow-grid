<script>
  import c from 'spencer-color'
  import { parts } from './store.js'
  export let color = 'steelblue'
  export let count = 10
  export let label = ''
  let colors = c.colors
  parts.update(arr => {
    arr.push({
      color: colors[color] || color,
      count: count,
      label: label,
    })
    return arr
  })
</script>

<style>

</style>

<div />
