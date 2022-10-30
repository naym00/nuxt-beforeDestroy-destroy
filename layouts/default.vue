<template>
  <v-app>
    <nav-bar :links="links"/>
    <Nuxt />
  </v-app>
</template>

<script>
import NavbarComponentVue from '~/components/NavbarComponent.vue';
export default {
  data(){
    return {
      links: [
        {to: '/test1', name: 'Test 1'},
        {to: '/test2', name: 'Test 2'}
      ]
    }
  },
  components: {
    'nav-bar': NavbarComponentVue
  },
  name: 'DefaultLayout',
}
</script>
