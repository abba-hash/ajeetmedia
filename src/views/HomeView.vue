<template>
  <main class="main">
    <HeroVue/>
    <AboutVue/>
    <SecurityVue/>
    <ServicesVue/>
    <AppMarket/>
    <SubscribeVue/>
  </main>
</template>

<script>
// @ is an alias to /src
import HeroVue from '@/components/Hero.vue'
import AboutVue from '@/components/About.vue'
import SecurityVue from '@/components/Security.vue'
import ServicesVue from '@/components/Services.vue'
import AppMarket from '@/components/AppMarket.vue'
import SubscribeVue from '@/components/Subscribe.vue'


export default {
  name: 'HomeView',
  components: {
    HeroVue,
    AboutVue,
    SecurityVue,
    ServicesVue,
    AppMarket,
    SubscribeVue
  }
}
</script>
