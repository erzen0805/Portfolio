<script>
  import Project from "./Project.svelte";
</script>

<Project name="전력설비 예방진단 시스템" imgSrc={["img/career/tds_ypp.jpg"]}>
  <h4 class="title">프로젝트 설명</h4>
  <div class="content">
    <p class="contents-normal">
      한국전력공사(KEPCO), 코레일에서 운영하는 전력 설비의 안전 및 신뢰성을 평가하기 위한 시스템입니다.
    </p>
    <p class="contents-normal">
      발전소, 변전소, 전력선로 등의 시설물을 모니터링하고, 잠재적인 문제를 조기에 탐지하여 사고나 장애의 발생을 예방하고자 개발되었습니다.
    </p>
    <p class="contents-normal">
      시스템은 데이터를 수집하고 분석한 결과를 시각화하고 경고나 알림을 보내어 운영자들이 조치를 취할 수 있도록 합니다.
    </p>
    <span class="contents-strong">신규프로젝트 중도참여 | 4인(PM, PM, BE, 막내) | 막내로 참여</span>
  </div>
  <h4 class="title">수행 업무</h4>
  <div class="content">
    <p class="contents-normal">
      화면기획, Restful API 정의, Front-end 개발, 진단알고리즘 개발, 부분방전파형관리도구 개발
    </p>
    <p class="contents-strong">
      언어 - .NET WPF | Vanilla JS | Python
    </p>
    <p class="contents-strong">
      기타 - HTTP | Keras | IEC61850 | MSSQL | Sqlite
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