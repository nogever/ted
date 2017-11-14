<template>
  <div id="app">
    <header>
      <app-header></app-header>
    </header>
    <main>
      <router-view></router-view>
    </main>
    <app-footer></app-footer>
  </div>
</template>

<script>
import AppHeader from '@/components/app-header'
import AppFooter from '@/components/app-footer'

export default {
  name: 'app',
  components: { AppHeader, AppFooter }
}
</script>

<style>
* { margin: 0; padding: 0; box-sizing: border-box; }
a { text-decoration: none; color: currentColor; }
ul, ol { list-style-type: none; }
body {
  font-family: 'HelveticaNeue-Light', 'Helvetica Neue Light', 'Helvetica Neue', Helvetica, Arial, 'Lucida Grande', sans-serif; 
  font-weight: 300;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
