# shayna

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Note
pada vue js beberapa library js tidak dapat di gunakan (ditimpa) ex carousel
solusi: install plugin din vue ui (vue-owl-carousel)

## Menggunakn vue-owl-carousel

-install dependensi  [vue-owl-carousel](https://github.com/s950329/vue-owl-carousel)
```
import carousel from 'vue-owl-carousel
exsport default {
    components:{carousel}
    }
```


## js lib
Carousel Owl

## Plugin
View route

## Slicing component agar reuseable [See](shayna/src/components)
buat template pada components
```
(shayna/src/components/HeaderShayna.vue)
```
tambahkan script
```
<script>
    export default{
        name: 'HeaderShayna'
    }
</script>
```
ubah template,script(components) dan import file HeaderShayna pada home.vue sebagai parent, 
```
<template>
  <div class="home">
    <HeaderShayna/>
  </div>
</template>
<script>
import HeaderShayna from '@/components/HeaderShayna.vue'
export default {
  name: 'Home',
  components: {
      HeaderShayna
  }
}
</script>
```
## Regitrasi view
- baut file view
- daftarkan di route pada file index.js kemudia impor dan regitrasikan
```
import Product from '../views/Product.vue'
```
```
{
    path: '/product',
    name: 'Product',
    component: Product
  },
```
##  Manupulasi [VUE DOM](https://medium.com/@MFaridZia/kenalan-dengan-vue-js-sebuah-framework-javascript-yang-keren-c0a0b272a148)
### ~(v-bind)

ex pada file [product.vue]() tambah kan property data() dan var di  tag script
```
export default {
  name: 'Product',
  components: {
    HeaderShayna,
    Footer,
    carousel
  },
  data(){
      return{
          gambar_default:"img/mickey2.jpg"
      }
  }
};
```
pangil var di html dengan v-bind / :
```

<div class="product-pic-zoom">
<img class="product-big-img" :src="gambar_default" alt="" />
</div>
```
### ~(v-bind)

