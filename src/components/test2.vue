<template>
  <div class="hello">
 <div class="card" style="width: 18rem;">
  <img v-if="check" v-bind:src="foto" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">{{check}}</h5>
    <p class="card-text">{{msg}}</p>
    <button v-on:click="show" type="button" class="btn btn-primary">{{msgBtn}}</button>
  </div>
</div>
  </div>
</template>
 
<script>
/* eslint-disable */
export default {
  name: 'test2',
  props: {
    msg: String,
    foto: String
  },
  methods:{
    show(){
      this.check = ! this.check
      if(this.check == true){
        this.msgBtn = "Скрыть"
      }else{
        this.msgBtn = "Показать"
      }
    }
  },
  data(){
    return{
      check: true,
      msgBtn: "Скрыть"
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
