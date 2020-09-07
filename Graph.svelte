<script>
  import { Grid, Part } from './src'
</script>

<style>
  .link {
    color: steelblue;
    text-decoration: none;
    margin: 4rem;
    font-size: 1.5rem;
  }
</style>

<div style="width:50%; margin:4rem;">
  <div style="margin:3rem; font-size:1.5rem; color:steelblue;">
    <a class="link" href="https://github.com/spencermountain/somehow-grid">somehow-grid</a>
  </div>
  <Grid total="500" size="15">
    <Part color="orange" count="100" />
    <Part color="sky" count="200" label="blue" />
    <Part color="rose" count="100" label="rose" />
  </Grid>
</div>
