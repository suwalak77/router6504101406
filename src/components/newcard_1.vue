<template>
    <div class="box_all">
    <div class="col" v-for="(n,i) in travelList" :key="n">
      <div class="card" style="width: 25rem;" >
        <img :src="n.img" class="card-img-top">
        <div class="card-body">
          <h3 class="card-title">{{ n.name }}</h3>
          <p>BookingPrice : {{n.price}}</p>
          <h6>Open: 8.00-19.00 </h6>
          

          <a class="btn btn-primary" @click="list_local_control(i.name, i.quantity)"> Booking </a>
        </div>
      </div>
    </div>
  </div>

</template>

<script setup>

import { ref } from 'vue';

const travelList=ref([
    {name: 'HANNAH HAHN',  price:70, img:"https://chiangmaicheckin.com/pic/cover/s84.jpg", quantity: 0 ,
        text_box:' Location: https://maps.app.goo.gl/9u4WXLjQoQfRNobr8'
    }])


</script>

<style>

.card-img-top{
height: 100%;
padding: 25px;
border-radius: 60px;


}
.box_all{
justify-content: center;
align-items: center;
margin-left: 30%;
text-align: center;
border-radius: 60px;

}
.btn.btn-primary{
background-color: rgb(0, 0, 0);
}

</style>