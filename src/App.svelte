<script>
  import Menu from './Menu.svelte';
  import Intro from './page/intro/Index.svelte';
  import About from './page/about/Index.svelte';

  const menuWidth = "100px";
</script>

<Menu style="width: {menuWidth};"/>
<div style="margin-left: {menuWidth}; overflow: hidden;">
  <Intro/>
  <About/>
</div>