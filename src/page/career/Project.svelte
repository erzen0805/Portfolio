<script>
  import { fade } from 'svelte/transition';

  export let name;
  export let imgSrc;
</script>

<div class="root" in:fade>
  <h3 class="name">{name}</h3>
  {#if !!imgSrc}
  <div style="text-align: center;">
    {#each imgSrc as src}
    <img src={src} alt={name}/>
    {/each}
  </div>
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
  max-height: 190px;
  margin-right: 4px;
}
</style>