<script>
  export let source;
  export let title;
</script>

<div class="container">
  <img src={source} alt={title}>
  <div class="title">{title}</div>
</div>

<style>
.container {
  width: 6vw;
  height: 8vw;
  /* border: 3px solid green; */
}
img {
  width: 100%;
  height: 6vw;
  border: 3px solid gold;
  border-radius: 20%;
}
.title {
  font-family: KoHo;
  font-size: 1rem;
  color: rgb(193, 193, 193);
  text-align: center;
  margin-top: 3px;
}
</style>