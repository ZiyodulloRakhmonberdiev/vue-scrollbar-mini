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
    </main>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {

  },
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
    flex-direction: column;
    justify-content: space-between;
    height: 10vh;
    width: 100%;
    align-items: center;
  }
  header h1{
    color: #fff;
    font-size: 32px;
  }
</style>
