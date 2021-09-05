<template>
  <article class="">
    <div class="content">
      <h2>Burger </h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
      </p>
      <h2>Burger </h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
      </p>
      <h2>Burger </h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
      </p>
      <h2>Burger </h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
      </p>
      <h2>Burger </h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
      </p>
    </div>
  </article>
</template>
<script>
export default {
  name: 'post',
  mounted(){
    this.$el.addEventListener('scroll', function() {
      let scrollTop = this.$el.scrollTop;
      let clientHeight = this.$el.clientHeight;
      let scrollHeight = this.$el.scrollHeight;
      let scrollPercent = Math.round((scrollTop) / (scrollHeight - clientHeight)* 100);
      this.$emit('progressUpdate', scrollPercent)
    }.bind(this));
  }
}
</script>
<style media="screen">
  article{
    width: 100%;
    flex: 1 1 100%;
    max-height: calc(100vh - 80px);
    overflow: scroll;
    background: #adaaa1;
  }
  .content{
    display: flex;
    justify-content: center;
    padding: 30px 100px;
    background: #eee;
    flex-direction: column;
  }
  .content h2{
    font-size: 32px;
    font-weight: bold;
    margin-bottom: 10px;
    color: brown;
  }
  .content p{
    font-size: 22px;
    color: #313131;
    font-weight: 300;
    line-height: 1.5;
    margin-bottom: 15px;
  }
</style>
