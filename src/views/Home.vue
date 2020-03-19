<template>
  <div class="home">
    <HeaderShayna/>
    <HeroShayna/>
    <WomanShayna/>

    <Instagram/>
    <Logo/>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderShayna from '@/components/HeaderShayna.vue'
import HeroShayna from '@/components/HeroShayna.vue'
import WomanShayna from '@/components/WomanShayna.vue'
import Instagram from '@/components/InstaShayna.vue'
import Logo from '@/components/Partner.vue'
import Footer from '@/components/Footer.vue'



export default {
  name: 'Home',
  components: {
    HeaderShayna,
    HeroShayna,
    WomanShayna,
    Instagram,
    Logo,
    Footer
  }
};
</script>
