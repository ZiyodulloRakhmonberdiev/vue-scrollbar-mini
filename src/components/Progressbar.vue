<template>
  <div class="progress_bar">
    <div :class="(progress === 100) ? 'progress_inner complete': 'progress_inner'"
    :style="`width: ${progress}%`">
      <span class="white"> {{progress}}%</span>
    </div>
  </div>
</template>
<script type="text/javascript">
  export default {
    name: 'progressbar',
    props: ['progress']
  }
</script>
<style>
  .progress_bar{
    width: 100%;
    height: 20px;
    background: #002a3a;
    position: relative;
  }
  .progress_inner{
    height: 100%;
    background: linear-gradient(to right, #ed008d, #2484e4);
    border-radius: 0 10px 10px 0;
  }
  .progress_inner span{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 14px;
    color: #111;
  }
  .dark{
    color: #111;
  }
  .progress_inner span.white{
    color: #fff;
  }
  .complete{
    border-radius: 0;
  }
</style>
