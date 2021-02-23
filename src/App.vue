<template>
  <div id="app">
    <HeaderComponent />
    <SectionComponent />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from '@/components/Header/index'
import SectionComponent from '@/components/Section-Body/index'
import FooterComponent from '@/components/Footer/index'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    SectionComponent,
    FooterComponent
  }
}
</script>

<style lang="scss" scoped>
  #app{
    display: grid;
    grid-template-rows: 100vh auto 2000px;
    grid-template-areas: 'HD' 'BD' 'FT';
  }
</style>
