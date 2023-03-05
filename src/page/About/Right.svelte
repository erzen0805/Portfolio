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
    <ImageBox imgSource="./src/assets/c.png" imgTitle="C++" />
    <ImageBox imgSource="./src/assets/mfc.png" imgTitle="MFC" />
    <ImageBox imgSource="./src/assets/qt.png" imgTitle="QT C++" />
    <ImageBox imgSource="./src/assets/dotnet.png" imgTitle="C#" />
    <ImageBox imgSource="./src/assets/wpf.png" imgTitle="WPF" />
    <ImageBox imgSource="./src/assets/dotnetcore.png" imgTitle=".NET CORE" />
    <ImageBox imgSource="./src/assets/java.png" imgTitle="Java" />
    <ImageBox imgSource="./src/assets/go.png" imgTitle="GO" />
    <ImageBox imgSource="./src/assets/python.png" imgTitle="Python" />
    <ImageBox imgSource="./src/assets/jupyter_notebook.png" imgTitle="J-Notebook" />
    <ImageBox imgSource="./src/assets/keras.png" imgTitle="Keras" />

    <ImageBox imgSource="./src/assets/html.png" imgTitle="HTML5" />
    <ImageBox imgSource="./src/assets/css.png" imgTitle="CSS" />
    <ImageBox imgSource="./src/assets/js.png" imgTitle="JavaScript" />
    <ImageBox imgSource="./src/assets/jquery.png" imgTitle="jQuery" />
    <ImageBox imgSource="./src/assets/es6.png" imgTitle="ES6" />
    <ImageBox imgSource="./src/assets/svelte.png" imgTitle="Svelte.js" />
    <ImageBox imgSource="./src/assets/react.png" imgTitle="React.js" />
    <ImageBox imgSource="./src/assets/vue.png" imgTitle="Vue.js" />
    <ImageBox imgSource="./src/assets/vite.png" imgTitle="Vite" />

    <ImageBox imgSource="./src/assets/github.png" imgTitle="GitHub" />
    <ImageBox imgSource="./src/assets/bitbucket.png" imgTitle="Bitbucket" />

    <ImageBox imgSource="./src/assets/redmine.png" imgTitle="Redmine" />
    <ImageBox imgSource="./src/assets/git.png" imgTitle="Git" />
    <ImageBox imgSource="./src/assets/iec61850.png" imgTitle="IEC61850" />
    <ImageBox imgSource="./src/assets/jira.png" imgTitle="Jira" />
    <ImageBox imgSource="./src/assets/modbus.png" imgTitle="MODBUS" />
    <ImageBox imgSource="./src/assets/mssql.png" imgTitle="MSSQL" />
    <ImageBox imgSource="./src/assets/mysql.png" imgTitle="MySQL" />
    <ImageBox imgSource="./src/assets/notion.png" imgTitle="Notion" />
    <ImageBox imgSource="./src/assets/oracle.png" imgTitle="OracleDB" />
    <ImageBox imgSource="./src/assets/redis.png" imgTitle="Redis" />
    <ImageBox imgSource="./src/assets/sqlite.png" imgTitle="SQLite" />
    <ImageBox imgSource="./src/assets/svn.png" imgTitle="SVN" />
    <ImageBox imgSource="./src/assets/tcp.png" imgTitle="TCP/IP" />
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