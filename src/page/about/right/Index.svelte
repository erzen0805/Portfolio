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
  <div class="category">
    <ul>
      <li class:selected={viewPage===0} on:click|preventDefault={()=>onContentsChangeClick(0)}>- Languages</li>
      <li class:selected={viewPage===1} on:click|preventDefault={()=>onContentsChangeClick(1)}>- Web FE</li>
      <li class:selected={viewPage===2} on:click|preventDefault={()=>onContentsChangeClick(2)}>- Collaboration Tools</li>
      <li class:selected={viewPage===3} on:click|preventDefault={()=>onContentsChangeClick(3)}>- ETC</li>
    </ul>
  </div>
  <div class="parent">
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
  </div>
</section>

<style>
.container {
  width: 90%;
  height: 480px;
  margin-top: 100px;
  padding: 0 30px 0 10px;
  background-color: rgb(76, 76, 76);
  display: inline-block;
  position: relative;
}
.container::after {
  transform: skewX(0.3deg) rotateZ(-7deg);
  content: "";
  width: 110%;
  height: 90%;
  background-color: rgb(46, 46, 46);
  position: absolute;
  top: 40px;
  box-shadow: rgb(0 0 0 / 50%) 0px 4px 24px;
}
@media (min-height: 480px) {
  .container {
    height: 100%;
  }
}
.category {
  transform: skewX(0.3deg) rotateZ(-7deg);
}
.category li {
  margin-right: 20px;
  font-size: 1.25rem;
  color: rgb(158, 158, 158);
  cursor: pointer;
  display: inline;
}
.category .selected {
  color: rgb(245, 210, 14);
}
.parent {
  display: flex;
  align-items: flex-start;
  z-index: 1;
  position: relative;
  width: 95%;
  left: 10%;
  top: 13%;
  height: 80%;
  overflow-y: auto;
}
.contents {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  width: 100%;
  padding: 3px;
}
</style>