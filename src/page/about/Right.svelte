<script>
  import Languages from './Languages.svelte';
  import WebFE from './WebFE.svelte';
  import CollaborationTools from './CollaborationTools.svelte';
  import ETC from './ETC.svelte';

  let viewPage = 0;
  function onContentsChangeClick(pageIndex) {
    viewPage = pageIndex;
  }
</script>

<section class="container">
  <div class="rotate">
    <ul>
      <li class:selected={viewPage===0} on:click|preventDefault={()=>onContentsChangeClick(0)}>- Languages</li>
      <li class:selected={viewPage===1} on:click|preventDefault={()=>onContentsChangeClick(1)}>- Web FE</li>
      <li class:selected={viewPage===2} on:click|preventDefault={()=>onContentsChangeClick(2)}>- Collaboration Tools</li>
      <li class:selected={viewPage===3} on:click|preventDefault={()=>onContentsChangeClick(3)}>- ETC</li>
    </ul>
  </div>
  <div class="contents">
    {#if viewPage === 0}
    <Languages />
    {/if}
    {#if viewPage === 1}
    <WebFE />
    {/if}
    {#if viewPage === 2}
    <CollaborationTools />
    {/if}
    {#if viewPage === 3}
    <ETC />
    {/if}
  </div>
</section>

<style>
.container {
  margin-top: 100px;
  padding: 0 30px 0 10px;
  background-color: rgb(76, 76, 76);
  width: 90%;
  height: calc(100vh - 170px);
  position: relative;
}
.rotate {
  transform: skewX(0.3deg) rotateZ(-7deg);
}
.rotate li {
  margin-right: 20px;
  font-size: 1.25rem;
  color: rgb(158, 158, 158);
  cursor: pointer;
  display: inline;
}
.rotate::after {
  content: "";
  width: 150vh;
  height: calc(100vh - 170px);
  background-color: rgb(46, 46, 46);
  position: absolute;
  top: 40px;
  box-shadow: rgb(0 0 0 / 50%) 0px 4px 24px;
}
.contents {
  z-index: 1;
  position: relative;
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  /* border: 3px solid green; */
  width: 90%;
  max-height: calc(100vh - 310px);
  left: 9vw;
  top: 9vh;
  overflow-y: auto;
}
.rotate .selected {
  color: rgb(245, 210, 14);
}
</style>