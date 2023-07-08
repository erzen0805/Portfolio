<script>
  import { fade } from 'svelte/transition';

  export let source;
  export let title;

  let imageDown = false;
  function handleMouseOver(value) {
    imageDown = value;
  }
  
  let showPopup = false;
  
</script>

<div class="container" on:mouseover={()=>handleMouseOver(true)} on:mouseout={()=>handleMouseOver(false)} in:fade>
  <img src={source} alt={title} class:mouseover={imageDown} >
  <div class="title">{title}</div>
</div>

<style>
.container {
  color: rgb(193, 193, 193);
  width: 6vw;
  height: 8vw;
  margin-bottom: 15px;
  position: relative;
  /* border: 3px solid green; */
}
img {
  display: inline-block;
  width: 100%;
  height: 6vw;
  border: 3px solid gold;
  border-radius: 20%;
}
.title {
  font-family: KoHo;
  font-size: 1rem;
  text-align: center;
  margin-top: 5px;
}
.mouseover {
  animation: 0.3s ease 0s 1 alternate forwards running movement;
}
@keyframes movement {
  from {
    margin-top: 0px;
    transform: scale(1);
  }
  to {
    margin-top: 3px;
    transform: scale(0.98);
  }
}
</style>