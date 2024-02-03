<template>
<div class="rows">

  <div class="row g-3">
    <div class="col-auto">
        <label for="inputName" class="visually-hidden">Название</label>
        <input type="text" v-model="part.PName"  class="form-control" id="inputName" >
    </div>
    <div class="col-auto">
        <label for="inputPrice" class="visually-hidden">Цена за шт</label>
        <input type="text"  v-model="part.Pprice" class="form-control" id="inputPrice" placeholder="Цена за шт">
    </div>
    <div class="col-auto">
        <label for="inputVolum" class="visually-hidden">Кол-во</label>
        <input type="text" v-model="part.PVolum" class="form-control" id="inputVolum" placeholder="Кол-во">
    </div>
    <div class="col-auto">
      <button @click="add" class="btn btn-primary mb-3">Добавить</button>
    </div>
  </div>

  <div class="col-auto">
    <button v-on:click="show" class="btn btn-primary mb-3">Паказать</button>
  </div>

  <div v-if="check" >
    <div v-for="item in productCart" :key="item" class="alert alert-primary" role="alert">
      Наименование : {{item.PName}} <br/>
      Цена         : {{item.Pprice}} <br/>
      Bec          : {{item.PVolum}}
    </div>
  </div>


</div>
</template>
 
<script>
/* eslint-disable */

import Product from '@/components/Product.js'
export default {
  name: 'Card',
  props: {
    msg: String
    
  },
  data(){
    return{
      part: Product,
      productCart: [],
      check: false
    }
  },
  methods:{
    add(){
      this.productCart.push({...this.part})
      this.part.PName = '';
      this.part.Pprice = '';
      this.part.PVolum = '';
    },
    show(){
      this.check = !this.check;
    }
  }
}
</script>

