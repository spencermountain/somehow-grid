<div align="center">
  <div><b>somehow-grid</b></div>
  <img src="https://user-images.githubusercontent.com/399657/68222691-6597f180-ffb9-11e9-8a32-a7f38aa8bded.png"/>
  <div>— part of <a href="https://github.com/spencermountain/somehow">somehow</a> —</div>
  <div>WIP svelte infographics</div>
  <div align="center">
    <sub>
      by
      <a href="https://spencermounta.in/">Spencer Kelly</a> 
    </sub>
  </div>
</div>
<div align="right">
  <a href="https://npmjs.org/package/somehow-grid">
    <img src="https://img.shields.io/npm/v/somehow-grid.svg?style=flat-square" />
  </a>
</div>
<img height="25px" src="https://user-images.githubusercontent.com/399657/68221862-17ceb980-ffb8-11e9-87d4-7b30b6488f16.png"/>

a svelte component to render a bunch of squares, and color some of them

work-in-progress,

`npm i somehow-grid`

```html
<script>
  import { Grid, Part } from 'somehow-grid'
</script>

<Grid total="500">
  <Part color="red" count="100" />
  <Part color="blue" count="100" />
</Grid>
```

![image](https://user-images.githubusercontent.com/399657/92409898-30e05380-f110-11ea-965c-b8e7d4c1cb25.png)

MIT
