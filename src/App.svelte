<script>
  import Menu from './Menu.svelte';
  import Home from './page/Home.svelte';
  import About from './page/About.svelte';

  const menuWidth = "100px";
</script>

<Menu style="width: {menuWidth};"/>
<div style="margin-left: {menuWidth}; overflow: hidden;">
  <Home/>
  <About/>
</div>