<script>
  export let imgSource;
  export let imgTitle;
</script>

<div class="container">
  <img src={imgSource} alt={imgTitle}>
  <div class="title">{imgTitle}</div>
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