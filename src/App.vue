<template>
  <div id="app">
    <Header/>
    <Categories/>

    <router-link to="/">List</router-link>
    <router-link to="/detail">Detail</router-link>
    <router-view></router-view>
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Categories from './components/Types.vue'

export default {
  name: 'App',
  components: {
    Header,
    Categories
  }
}
</script>

