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

![image](https://user-images.githubusercontent.com/399657/83908152-9baa7900-a734-11ea-8f86-5a8efba30418.png)

MIT
