<script>
  import { fade, fly } from 'svelte/transition';
  import Languages from './Languages.svelte';
  import WebFE from './WebFE.svelte';
  import CollaborationTools from './CollaborationTools.svelte';
  import ETC from './ETC.svelte';
</script>

<section class="container" in:fly={{ y: 200, duration: 1000 }} out:fade>
  <div class="rotate">
    <div>
      <span>- Languages</span>
      <span>- Web FE</span>
      <span>- Collaboration Tools</span>
      <span>- ETC</span>
    </div>
  </div>
  <div class="contents">
    <Languages />
    <WebFE />
    <CollaborationTools />
    <ETC />
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
.rotate span {
  margin-right: 20px;
  font-size: 1.25rem;
  color: rgb(245, 210, 14);
  /* color: rgb(158, 158, 158); */
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
  height: calc(100vh - 310px);
  left: 9vw;
  top: 9vh;
  overflow-y: scroll;
}
</style>