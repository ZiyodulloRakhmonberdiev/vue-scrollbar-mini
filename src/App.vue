<template>
  <div id="app">
    <main>
      <div class="navigation">
        <header>
          <h1>Samar Badriddinov</h1>
        </header>
        <nav>
          <a href="#">About</a>
          <a href="#">Contact</a>
          <a href="#">Portfolio</a>
        </nav>
      </div>
      <Progressbar :progress="progress"/>
      <Post @progressUpdate = "setProgress"/>
    </main>
  </div>
</template>

<script>
import Post from './components/Post'
import Progressbar from './components/Progressbar'
export default {
  name: "App",
  components: {
    Post,
    Progressbar
  },
  data(){
    return{
      progress: 0
    }
  },
  methods: {
    setProgress(progress){
      this.progress = progress;
    }
  }
};
</script>

<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body{
    font-family: 'monospace'. sans-serif;
  }
  main{
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    overflow: hidden;
  }
  .navigation{
    display: flex;
    justify-content: space-between;
    height: 10vh;
    width: 100%;
    align-items: center;
    background: #002333;
    padding: 30px;
    position: relative;
  }
  .navigation a{
    margin: 0 20px;
    text-decoration: none;
    color: #fff;
  }
  header h1{
    color: #fff;
    font-size: 32px;
  }
</style>
