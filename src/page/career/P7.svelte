<script>
  import Project from "./Project.svelte";
</script>

<Project name="SCADA" imgSrc={["img/career/autonics_scada.png", "img/career/autonics_scada2.jpg"]}>
  <h4 class="title">프로젝트 설명</h4>
  <div class="content">
    <p class="contents-normal">
      SCADA는 "Supervisory Control and Data Acquisition"의 약자로, 시스템 제어와 데이터 수집을 위한 통신 기술을 통합하는 시스템입니다.
    </p>
    <p class="contents-normal">
      SCADA 시스템은 네트워크를 통해 분산된 제어 장치와 통신하여 실시간으로 데이터를 모니터링하고 제어합니다.
    </p>
    <p class="contents-normal">
      신뢰성과 안정성이 요구되는 환경에서 널리 사용되며, 에너지, 제조, 수도 등 다양한 산업 분야에서 활용됩니다.
    </p>
    <span class="contents-strong">신규프로젝트 | 10인(PM, QT C++:8, PLC통신, 웹) | 웹 개발자로 참여</span>
  </div>
  <h4 class="title">수행 업무</h4>
  <div class="content">
    <p class="contents-normal">
      웹 일괄, SCADA화면 웹동기화, Kernal 모니터링/제어
    </p>
    <p class="contents-strong">
      언어 - React.js | GoLang | QT C++ | Python
    </p>
    <p class="contents-strong">
      기타 - HTTP | Sqlite
    </p>
  </div>
</Project>

<style>
.title {
  font-size: 1.2rem;
  font-weight: 600;
  color: white;
  margin: 40px 0 0 20px;
}
.content {
  margin: 20px 10px 0px 10px;
}
.contents-strong {
  color: rgb(146, 146, 146);
  font-weight: 700;
  font-size: 1.1rem;
  line-height: 1.7;
}
.contents-normal {
  font-size: 1.05rem;
  font-weight: 400;
  color: rgb(213, 213, 213);
  line-height: 1.7;
}
</style>