<script>
  import { fly, fade } from 'svelte/transition';

  export let name;
  export let imgSrc;

  let isImgVisible = false;

  function toggleImg() {
    isImgVisible = !isImgVisible;
  }
</script>

<div class="root" in:fade>
  <h3 class="name">{name}</h3>
  {#if !!imgSrc}
  <button on:click={toggleImg} class="button">
    {isImgVisible ? '관련 이미지 숨기기' : '관련 이미지 보기'}
  </button>
    {#if !!imgSrc && isImgVisible}
    <div style="text-align: center; margin-top: 5px;" transition:fly>
      {#each imgSrc as src}
      <img src={src} alt={name}/>
      {/each}
    </div>
    {/if}
  {/if}
  <slot />
</div>

<style>
.root {
  padding: 20px 20px 40px 20px;
  font-family: KoHo;
  font-size: 1.25rem;
  font-weight: 700;
  color: rgb(146, 146, 146);
}
.button {
	box-shadow:inset 0px 1px 0px 0px #ffffff;
	background:linear-gradient(to bottom, #f9f9f9 5%, #e9e9e9 100%);
	background-color:#f9f9f9;
	border-radius:9px;
	border:1px solid #dcdcdc;
	display:inline-block;
	cursor:pointer;
	color:#666666;
	font-family:Arial;
	font-size:15px;
	font-weight:bold;
	padding:8px 50px;
	text-decoration:none;
	text-shadow:0px 4px 8px #ffffff;
  display: block;
  width: 90%;
  margin: 0 auto;
}
.button:hover {
	background:linear-gradient(to bottom, #e9e9e9 5%, #f9f9f9 100%);
	background-color:#e9e9e9;
}
.button:active {
	position:relative;
	top:1px;
}
.name {
  font-size: 1.8rem;
  font-weight: 700;
  margin-bottom: 15px;
  display: flex;
  flex-direction: column;
  color: rgb(184, 232, 41);
}
img {
  border-radius: 10px;
  width: 80%;
}
</style>