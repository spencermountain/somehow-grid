<script>
  export let color = 'steelblue'
  export let count = 10

  import { parts } from './store.js'
  parts.update(arr => {
    arr.push({
      color: color,
      count: count,
    })
    return arr
  })
</script>

<style>

</style>

<div />
