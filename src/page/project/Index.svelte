<script>
  import { fly } from 'svelte/transition';
  import { inview } from 'svelte-inview';

  let stylish=$$props.style;

  let isInView = false;
  const viewCondition = { unobserveOnEnter: false, rootMargin: '-200px' };
  const onViewChange = ({detail}) => {
    isInView = detail.inView;
  };

  let viewPage = 0;
  function onChangePage(pageIndex) {
    viewPage = pageIndex;
  }

  const projects = [
    {title: "재직중 (1.4년)", company: "전력설비 예방진단 | 비츠로시스"},
    {title: "~2022 (1.2년)", company: "전력설비 예방진단 | YPP"},
    {title: "~2021 (1.0년)", company: "SCADA | 오토닉스"},
    {title: "~2020 (1.2년)", company: "카카오 선물하기 서버 | 쿠프마케팅"},
    {title: "~2019 (0.5년)", company: "가상화폐 자동투자 봇 | 개인개발"},
    {title: "~2018 (1.3년)", company: "ATM/KIOSK 관리 서버 | 효성T&S"},
    {title: "~2017 (7.3년)", company: "전력설비 예방진단 | 유호전기공업"},
    {title: "~2014 (0.8년)", company: "전력 SCADA | 가보"},
    {title: "~2009 (1.0년)", company: "바다이야기 | 엔톤"},
    {title: "~2009", company: "컴퓨터공학과 학사 | 동명대학교"},
  ];
</script>

<main class="container" style={stylish} use:inview={viewCondition} on:change={onViewChange}>
  <div style="width: calc(100% - 500px); margin-bottom: 50px;">
  {#if isInView}
    <div class="contents" in:fly={{ y: 200, duration: 1000 }}>
      {#if viewPage === 0}
      <div>
        
      </div>
      {:else}
      <ETC />
      {/if}
    </div>
  {/if}
  </div>
  <div style="width: 500px;">
    <ul class="list">
      {#each projects as { title, company }, i}
      <li class:selected={viewPage===i} on:click|preventDefault={()=>onChangePage(i)}>
        <span class="label-left">{title}</span><span class="label-right">{company}</span>
      </li>
      {/each}
    </ul>
  </div>
</main>

<style>
.container {
  user-select: none;
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