<template>
  <div class="rows">
    <div class="input-group mb-3">
    <input v-model="userName" type="text" class="form-control" placeholder="Username" aria-label="Username" aria-describedby="basic-addon1">
</div>

    <button v-on:click="sendMsg" type="button" class="btn btn-danger">Нажать</button>

    <div class="rows">
    
    </div>
  </div>
</template>

<script>
/* eslint-disable */ 
export default {
  name: 'TestEmit',
  emits:['msg'],
  data(){
    return{
        userName: ''
    }
  },
  methods:{
    sendMsg(){
        this.$emit('msg', this.userName)
    }
  },
  inject:['animal']
}
</script>

