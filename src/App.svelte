<script>
  import Menu from './Menu.svelte';
  import Intro from './page/Intro.svelte';
  import About from './page/About/Index.svelte';

  const menuWidth = "100px";
</script>

<Menu style="width: {menuWidth};"/>
<div style="margin-left: {menuWidth}; overflow: hidden;">
  <Intro/>
  <About/>
</div>