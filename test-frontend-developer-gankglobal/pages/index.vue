<template>
  <div class="container">
<section class="hero">
  <div class="hero-body">
    <div class="container">
      <h1 class="title">
        Coctailspedia
      </h1>
      <h2 class="subtitle">
        This project using Nuxt.JS
      </h2>
    </div>
  </div>
</section>
<div class="panel">
  <div class="panel-heading">
    <div class="panel-block" v-for="coctail in coctails" :key="coctail.strDrink">
    {{coctails.drinks}}
    </div>
  </div>
</div>
  </div>
</template>

<script>
import axios from '~/plugins/axios'

export default{
  asyncData(){
      return axios.get('coctails')
      .then(res => ({
        coctails : res.data
      }))
  }
}
</script>

