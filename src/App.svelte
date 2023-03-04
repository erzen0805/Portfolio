<script>
  import Menu from './Menu.svelte';
  import Home from './Home.svelte';
  import About from './About.svelte';

  const menuWidth = "100px";
</script>

<Menu style="width: {menuWidth};"/>
<div style="margin-left: {menuWidth};">
  <Home/>
  <About/>
</div>