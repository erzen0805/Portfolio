<script>
  import { fade, fly } from 'svelte/transition';
</script>

<section style="margin-top: 100px; padding: 0 30px 0 10px; background-color: aquamarine; height: 500px;" in:fly={{ y: 200, duration: 1000 }} out:fade>
</section>

<style>
</style>