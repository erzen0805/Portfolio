<script>
  import { inview } from 'svelte-inview';
  import AboutLeft from './AboutLeft.svelte';
  import AboutRight from './AboutRight.svelte';
  
  let stylish=$$props.style;

  let isInView = false;
  const viewCondition = { unobserveOnEnter: false, rootMargin: '-300px' };
  const onViewChange = (event) => {
    //const { inView, entry, scrollDirection, observer, node} = event.detail;
    isInView = event.detail.inView;
  };
</script>

<main class="container" style={stylish} use:inview={viewCondition} on:change={onViewChange}>
  <div style="width: 40vw;">
    {#if isInView}
    <AboutLeft/>
    {/if}
  </div>
  <div style="width: 60vw;">
    {#if isInView}
    <AboutRight/>
    {/if}
  </div>
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