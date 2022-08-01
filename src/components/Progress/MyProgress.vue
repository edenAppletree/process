<template>
  <div class="progress">
    <div class="box">
      <div
        class="content"
        :class="{
          normal: status === 'normal',
          success: status === 'success',
          happy: status === 'happy',
          warning: status === 'warning',
        }"
        :style="{
            width:`${percentage}%`,
            backgroundColor:backgroundColor
        }"
      ></div>
    </div>
      <span class="num">{{percentage}}%</span>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    percentage: {
      type: String,
      default:'100'
    },
    status: {
      type: String
    },
    backgroundColor:{
        default:String,
        default:'orange'
    }
  },
  created() {},

  methods: {},
};
</script>

<style scoped>
.progress {
    display: flex;
    justify-content: start;
    margin: 20px 0;
}
.box {
  width: 300px;
  height: 20px;
  border-radius: 16px;
  border: 1px solid green;
}
.content {
  width: 60%;
  height: 100%;
  border-radius: 16px;
}
.num {
    margin-left: 5px;
    font-size: 16px;
}
.normal {
  background-color: skyblue !important;
}
.success {
  background-color: green !important;
}
.happy {
  background-color: pink !important;
}
.warning {
  background-color: red !important;
}
</style>
