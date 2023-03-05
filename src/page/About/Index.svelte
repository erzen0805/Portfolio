<script>
  import { fade, fly } from 'svelte/transition';
  import { inview } from 'svelte-inview';
  import Left from './Left.svelte';
  import Right from './Right.svelte';  

  let stylish=$$props.style;

  let isInView = false;
  const viewCondition = { unobserveOnEnter: false, rootMargin: '-300px' };
  const onViewChange = (event) => {
    //const { inView, entry, scrollDirection, observer, node} = event.detail;
    isInView = event.detail.inView;
  };
</script>

<main class="container" style={stylish} use:inview={viewCondition} on:change={onViewChange}>
  {#if isInView}
  <div style="width: 40vw;" in:fly={{ x: -200, duration: 1000 }} out:fade>
    <Left />
  </div>
  {/if}
  {#if isInView}
  <div style="width: 60vw;" in:fly={{ y: 200, duration: 1000 }} out:fade>
    <Right />
  </div>
  {/if}
</main>

<style>
.container {
  height: 100vh;
  display: flex;
  position: relative;  
  /* border: 3px solid green; */
  font-family: KoHo;
  user-select: none;
}
</style>