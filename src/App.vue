<template>
  <div id="app">
      <Header />
      <main>
        <ListaDischi />
      </main>
      
  </div>
</template>

<script>
import Header from './components/Header';
import ListaDischi from './components/ListaDischi'

export default {
  name: 'App',
  components:{
    Header,
    ListaDischi,
  }
} 

</script>

<style lang="scss">
  @import './style/general';
</style>
