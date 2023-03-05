<script>
  import { fade, fly } from 'svelte/transition';
  import ImageBox from './ImageBox.svelte';
</script>

<section class="container" in:fly={{ y: 200, duration: 1000 }} out:fade>
  <div class="rotate">
    <div>
      <span>Languages</span>
      <span>Collaboration tools</span>
    </div>
  </div>
  <div class="contents">
    <ImageBox source="./src/assets/c.png" title="C++" />
    <ImageBox source="./src/assets/mfc.png" title="MFC" />
    <ImageBox source="./src/assets/qt.png" title="QT C++" />
    <ImageBox source="./src/assets/winform.png" title=".NET WinForm" />
    <ImageBox source="./src/assets/wpf.png" title=".NET WPF" />
    <ImageBox source="./src/assets/dotnetcore.png" title=".NET CORE" />
    <ImageBox source="./src/assets/lightning_chart.png" title="LightningChart" />
    <ImageBox source="./src/assets/java.png" title="Java" />
    <ImageBox source="./src/assets/java_spring.png" title="Java Spring" />
    <ImageBox source="./src/assets/go.png" title="GO" />
    <ImageBox source="./src/assets/python.png" title="Python" />
    <ImageBox source="./src/assets/jupyter_notebook.png" title="J-Notebook" />
    <ImageBox source="./src/assets/keras.png" title="Keras" />

    <ImageBox source="./src/assets/html.png" title="HTML5" />
    <ImageBox source="./src/assets/css.png" title="CSS" />
    <ImageBox source="./src/assets/js.png" title="JavaScript" />
    <ImageBox source="./src/assets/jquery.png" title="jQuery" />
    <ImageBox source="./src/assets/es6.png" title="ES6" />
    <ImageBox source="./src/assets/svelte.png" title="Svelte.js" />
    <ImageBox source="./src/assets/react.png" title="React.js" />
    <ImageBox source="./src/assets/redux.png" title="Redux" />
    <ImageBox source="./src/assets/vue.png" title="Vue.js" />
    <ImageBox source="./src/assets/threejs.png" title="Three.js" />
    <ImageBox source="./src/assets/vite.png" title="Vite" />

    <ImageBox source="./src/assets/svn.png" title="SVN" />
    <ImageBox source="./src/assets/git.png" title="Git" />
    <ImageBox source="./src/assets/github.png" title="GitHub" />
    <ImageBox source="./src/assets/bitbucket.png" title="Bitbucket" />
    <ImageBox source="./src/assets/redmine.png" title="Redmine" />
    <ImageBox source="./src/assets/jira.png" title="Jira" />
    <ImageBox source="./src/assets/notion.png" title="Notion" />
    
    <ImageBox source="./src/assets/tcp.png" title="TCP/IP" />
    <ImageBox source="./src/assets/http.png" title="HTTP" />
    <ImageBox source="./src/assets/modbus.png" title="MODBUS" />
    <ImageBox source="./src/assets/iec61850.png" title="IEC61850" />
    <ImageBox source="./src/assets/mssql.png" title="MSSQL" />
    <ImageBox source="./src/assets/mysql.png" title="MySQL" />
    <ImageBox source="./src/assets/oracle.png" title="OracleDB" />
    <ImageBox source="./src/assets/redis.png" title="Redis" />
    <ImageBox source="./src/assets/sqlite.png" title="SQLite" />
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