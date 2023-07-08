<script>
  import { fade, fly } from 'svelte/transition';
  import { inview } from 'svelte-inview';
  import Left from './left/Index.svelte';
  import Right from './right/Index.svelte';  

  let stylish=$$props.style;

  let isInView = false;
  const viewCondition = { unobserveOnEnter: false, rootMargin: '-200px' };
  const onViewChange = ({detail}) => {
    //const { inView, entry, scrollDirection, observer, node} = event;
    isInView = detail.inView;
  };
</script>


<main class="root" style={stylish} use:inview={viewCondition} on:change={onViewChange}>
  <h2 style="display: none;">About</h2>
  <div class="container">
  {#if isInView}
  <div style="width: 40vw;" in:fly={{ x: -200, duration: 1000 }}>
    <Left />
  </div>
  <div style="width: 60vw; margin-bottom: 200px;" in:fly={{ y: 200, duration: 1000 }}>
    <Right />
  </div>
  {/if}
  </div>
</main>

<style>
.root {
  font-family: KoHo;
  user-select: none;
}
.container {
  height: 480px;
  display: inline-block;
  display: flex;
}
@media (min-height: 480px) {
  .container {
    height: 100vh;
  }
}
</style>