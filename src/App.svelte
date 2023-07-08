<script>
  import Menu from './Menu.svelte';
  import Intro from './page/intro/Index.svelte';
  import About from './page/about/Index.svelte';
  import Career from './page/career/Index.svelte';

  const menuWidth = "100px";
</script>

<h1 style="display: none;">Donghyun Lee's portfolio</h1>
<Menu style="width: {menuWidth};"/>
<div style="margin-left: {menuWidth}; overflow: hidden;">
  <Intro/>
  <About/>
  <Career/>
</div>