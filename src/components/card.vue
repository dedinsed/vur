<template>
<div class="rows">
<form class="row g-3">
  <div class="col-auto">
    <label for="staticEmail2" class="visually-hidden">Название</label>
    <input type="text" readonly class="form-control-plaintext" id="staticEmail2" value="email@example.com">
  </div>
  <div class="col-auto">
    <label for="inputPassword2" class="visually-hidden">Цена за шт</label>
    <input type="password" class="form-control" id="inputPassword2" placeholder="Цена за шт">
  </div>
   <div class="col-auto">
    <label for="inputPassword2" class="visually-hidden">Кол-во</label>
    <input type="password" class="form-control" id="inputPassword2" placeholder="Кол-во">
  </div>
  <div class="col-auto">
    <button type="submit" class="btn btn-primary mb-3">Confirm identity</button>
  </div>
</form>

  </div>
</template>
 
<script>
/* eslint-disable */
export default {
  name: 'card',
  props: {
    msg: String
    
  }
}
</script>

<
</style>
