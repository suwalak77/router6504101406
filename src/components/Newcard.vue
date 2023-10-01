<template>

    <div class="row mb-2">
            <div class="col-md-6" v-for="(n,i) in travelList" :key="n">
              <div class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative">
                <div class="col p-4 d-flex flex-column position-static">
                  <strong class="d-inline-block mb-2 text-primary-emphasis">Cafe NO. {{ i+1 }} </strong>
                  <h3 class="mb-0">{{n.name}}</h3>
                  <div class="mb-1 text-body-secondary">BookingPrice {{n.price}} baht</div>
                  <p class="card-text mb-auto">{{n.text_box}}</p>
                  
                  <div style="margin-bottom: 30px;">
                  <RouterLink :to="{name: `news_${i+1}` , params: {id: n.name}}" class="icon-link gap-1 icon-link-hover stretched-link">More information
                    <svg class="bi"> <use xlink:href="#chevron-right"/></svg>
                 </RouterLink>
                </div>     
                </div>
                <div class="col-auto d-none d-lg-block">
                  <svg class="bd-placeholder-img" width="200" height="250" xmlns="http://www.w3.org/2000/svg" role="img"  preserveAspectRatio="xMidYMid slice" focusable="false" 
                  style="margin: 15px;" >
                    <image :xlink:href="n.img" x="0" y="10" width="200" height="200" />
                  </svg>
                </div>
              </div>
            </div>
    
          
        </div>
    
</template>
    
    <script setup>
    import { RouterLink } from 'vue-router'
    import { ref } from 'vue';
    
    
    

    const travelList=ref([
       {name: 'HANNAH HAHN',  price:70, img:"https://chiangmaicheckin.com/pic/cover/s84.jpg", quantity: 0 ,
        text_box:' Location: https://maps.app.goo.gl/9u4WXLjQoQfRNobr8.'
        },
    
      {name:' No.39 Cafe',  price:65, img:"https://chiangmaicheckin.com/pic/cover/s5.jpg", quantity: 0 ,
        text_box:' Location: https://maps.app.goo.gl/mLkE4at6D2zf7BtDA'
        },
      
      {name:'Jaiboon', price:50, img:"https://chiangmaicheckin.com/pic/cover/s11.jpg", quantity: 0 ,
        text_box:'Location: https://maps.app.goo.gl/axATbFrQu9ZPmbzh8'
        },
    
      {name:'Fong nom',  price:49, img:"https://www.chiangmainews.co.th/wp-content/uploads/2022/09/29/2748665/1664423709_263948-chiangmainews.jpg", quantity: 0 ,
        text_box:'Location: https://maps.app.goo.gl/yocgi2AkoGWuVd4n8'
        },
    ])
    
    </script>
<style scoped>
</style>