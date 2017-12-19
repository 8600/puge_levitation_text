<template>
  <div class="levitation-text">
    <span v-for="item in text" :key="item">{{item}}</span>
  </div>
</template>

<script>
  export default {
    props: {
      text: String
    }
  }
</script>

<style lang='less' scoped>
  .levitation-text {
    text-align: center;
  }
  .levitation-text span {
    color: #fff;
    font-weight: bold;
    display: inline-block;
    letter-spacing: 5px;
    -webkit-transition: 2s;
    transition: 2s;
    text-shadow: 0px 0px 0px #677777;
    position: relative;
    top: 0px;
    left: 0px;
    cursor: default;
  }
  .levitation-text span:hover {
    text-shadow: -8px 8px 0px #677777;
    -webkit-transition: 0.3s;
    transition: 0.3s;
    top: -8px;
    left: 8px;
  }
  .levitation-text span.space {
    width: 20px;
    height: 100%;
  }
</style>