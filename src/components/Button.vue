<template>
  <div class="buttonDiv" ref="buttonDiv">
    <button @click="jump()">Clicky</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      y: 0,
      x: 0,
      color: "black",
      yPx: 0+"px",
      xPx: 0+"px"
    }
  },
  methods:{
    jump(){
      this.y=Math.round(Math.random() * (this.$refs.buttonDiv.clientHeight))
      this.x=Math.round(Math.random() * (this.$refs.buttonDiv.clientWidth))
      this.yPx=this.y+"px"
      this.xPx=this.x+"px"
      //setTimeout(() => {  this.y=100;this.yPx=this.y+"px"; this.x=100;this.xPx=this.x+"px" }, 1000);
    }
  }
}
</script>

<style>
@import "../assets/main.css";
button {
  color: #222222;
  background-color: var(--primary-color);
  font-weight: bold;
  top: v-bind(yPx);
  left: v-bind(xPx);
}
.buttonDiv {
  width: 100vw;
  height: 80vh;
}
</style>