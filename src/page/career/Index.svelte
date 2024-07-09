<script>
  import { fly } from 'svelte/transition';
  import { inview } from 'svelte-inview';
  import P0 from './P0.svelte';
  import P1 from './P1.svelte';
  import P2 from './P2.svelte';
  import P3 from './P3.svelte';
  import P4 from './P4.svelte';
  import P5 from './P5.svelte';
  import P6 from './P6.svelte';
  import P7 from './P7.svelte';
  import P8 from './P8.svelte';
  import P9 from './P9.svelte';
  import UnderConstruction from '@/common/UnderConstruction.svelte';

  let stylish=$$props.style;

  let isInView = false;
  const viewCondition = { unobserveOnEnter: false, rootMargin: '-200px' };
  const onViewChange = ({detail}) => {
    isInView = detail.inView;
  };

  const projects = [
    {title: "재직중 (2.4년)", company: "전력설비 예방진단 | 비츠로시스"},
    {title: "~2022 (1.2년)", company: "전력설비 예방진단 | YPP"},
    {title: "~2021 (1.0년)", company: "SCADA | Autonics"},
    {title: "~2020 (1.2년)", company: "카카오 선물하기 서버 | 쿠프마케팅"},
    {title: "~2019 (0.5년)", company: "가상화폐 자동투자 봇 | 개인개발"},
    {title: "~2018 (1.3년)", company: "ATM/KIOSK 관리 서버 | 효성TNS"},
    {title: "~2017 (7.3년)", company: "전력설비 예방진단 | 유호전기공업"},
    {title: "~2014 (0.8년)", company: "전력 SCADA | 가보"},
    {title: "~2009 (1.0년)", company: "바다이야기 | 엔톤"},
    {title: "~2009", company: "컴퓨터공학과 학사 | 동명대학교"},
  ];

  let viewPage = projects.length - 1;
  function onChangePage(pageIndex) {
    viewPage = pageIndex;
  }
</script>

<main class="container" style={stylish} use:inview={viewCondition} on:change={onViewChange}>
  <h2 style="display: none;">Career</h2>
  <div style="width: calc(100% - 500px); margin-bottom: 50px;">
  {#if isInView}
    <div class="contents" in:fly={{ y: 200, duration: 1000 }}>
      {#if viewPage === 9}
        <P9/>
      {:else if viewPage === 8}
        <P8/>
      {:else if viewPage === 7}
        <P7/>
      {:else if viewPage === 6}
        <P6/>
      {:else if viewPage === 5}
        <P5/>
      {:else if viewPage === 4}
        <P4/>
      {:else if viewPage === 3}
        <P3/>
      {:else if viewPage === 2}
        <P2/>
      {:else if viewPage === 1}
        <P1/>
      {:else if viewPage === 0}
        <P0/>
      {:else}
        <UnderConstruction />
      {/if}
    </div>
  {/if}
  </div>
  <div style="width: 500px;">
    <ul class="list">
      {#each projects as { title, company }, i}
      <li 
        class:selected={viewPage===projects.length-i-1}
        on:click|preventDefault={()=>onChangePage(projects.length-i-1)}
        on:keypress|preventDefault={()=>onChangePage(projects.length-i-1)}
      >
        <span class="label-left">{title}</span><span class="label-right">{company}</span>
      </li>
      {/each}
    </ul>
  </div>
</main>

<style>
.container {
  display: flex;
  font-family: KoHo;
  font-size: 1.25rem;
  font-weight: 700;
  color: rgb(146, 146, 146);
}
.contents {
  width: 100%;
  background-color: rgb(43, 44, 42);
  border-radius: 25px;
  height: 80vh;
  box-shadow: rgb(0, 0, 0) 0px 0px 20px inset;
  overflow-y: auto;
}
@media (max-height: 500px) {
  .contents {
    height: 500px;
  }
}
.list {
  padding: 30px;
}
.list li {
  font-size: 1.10rem;
  color: rgb(158, 158, 158);
  cursor: pointer;
  margin-bottom: 30px;
}
.list li.selected {
  color: white;
  font-weight: 700;
  border-left: 5px solid pink; /* 왼쪽 선 스타일과 두께 설정 */
  position: relative;
  left: -5px;
}
.label-left {
  display: inline-block;
  width: 120px;
  margin-right: 20px;
  padding-left: 5px;
}
.label-right {
  display: inline-block;
  width: 280px;
}
</style>