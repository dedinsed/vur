<template>
  <div class="rows">
    <div class="alert alert-danger" role="alert">
      Сообщение : {{textmsg}}
    </div>
    <TestEmit v-on:msg="showMsg" />

  </div>
</template>

<script>
/* eslint-disable */ 
import TestEmit from '@/components/TestEmit.vue'
export default {
  name: 'card',
  components:{
    TestEmit
  },
  
  data(){
    return{
      textmsg:''
    }
  },
  methods:{
    showMsg(e){
        this.textmsg = `алпьлпьл ${e}`
    }
    
  }
}
</script>



