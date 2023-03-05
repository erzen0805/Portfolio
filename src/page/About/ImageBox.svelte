<script>
  export let imgSource;
  export let imgTitle;
</script>

<div style="width: 7vw; height: 9vw; background-color: red;">
  <img src={imgSource} alt={imgTitle}>
  <div>{imgTitle}</div>
</div>

<style>
.container {
}
</style>