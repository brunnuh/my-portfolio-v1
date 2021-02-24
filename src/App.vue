<template>
  <div id="app">
    <HeaderComponent />
    <SectionComponent />
    <PortifolioComponent />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from '@/components/Header/index'
import SectionComponent from '@/components/Section-Body/index'
import FooterComponent from '@/components/Footer/index'
import PortifolioComponent from '@/components/Portifolio/index'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    SectionComponent,
    PortifolioComponent,
    FooterComponent
  }
}
</script>

<style lang="scss" scoped>
  #app{
    display: grid;
    grid-template-rows: 100vh auto auto 200px;
    grid-template-areas: 'HD' 'BD' 'PF' 'FT';
  }
</style>
