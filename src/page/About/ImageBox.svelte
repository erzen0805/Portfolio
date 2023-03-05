<script>
  import { fade } from 'svelte/transition';

  export let source;
  export let title;
</script>

<div class="container" in:fade>
  <img src={source} alt={title}>
  <div class="title">{title}</div>
</div>

<style>
.container {
  width: 6vw;
  height: 8vw;
  margin-bottom: 15px;
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
  margin-top: 5px;
}
</style>