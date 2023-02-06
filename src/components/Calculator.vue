<template>
  <div class="home-container">
    <h1>Abi Schnitt</h1>
    <input type="number" placeholder="2.0" class="input" id="schnitt"/>
    <h1>Punkte Mathe</h1>
    <input type="number" placeholder="14.5" class="input" id="mathe"/>
    <h1>Punkte Deutsch</h1>
    <input type="number" placeholder="12.25" class="input" id="deutsch"/>
    <h1>Punkte Nat.Wis.</h1>
    <input type="number" placeholder="13" class="input" id="nat"/>
    <h1>Punkte Englisch</h1>
    <input type="number" placeholder="13.33" class="input" id="en"/>
    <div class="home-container1">
      <input type="checkbox" checked="true" class="home-checkbox" id="check"/>
      <span>Frühstudium etc.?</span>
    </div>
    <button class="button" @click="update">Berechnen</button>
    <span>{{points}}</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Home',
      points: 100,
      props: {}
    }
  },
  methods:{
    update(){
      this.points=((120-20*parseFloat(document.getElementById("schnitt").value))*0.65+0.35*Math.round(((parseFloat(document.getElementById("mathe").value)*3+parseFloat(document.getElementById("nat").value)*2+parseFloat(document.getElementById("deutsch").value)+parseFloat(document.getElementById("en").value))/7)*6+10))
      if(document.getElementById("check").checked===true){
        this.points+=2
      }
    }
  }
}
</script>

<style scoped>
.home-container {
  width: 100%;
  display: flex;
  overflow: auto;
  min-height: 100vh;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
.home-container1 {
  flex: 0 0 auto;
  width: auto;
  height: auto;
  display: flex;
  align-items: flex-start;
  justify-content: center;
}
.home-checkbox {
  align-self: center;
}
</style>