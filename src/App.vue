<template>
  <div id="app">
  <xyz-header>XYZ</xyz-header>
    <XyzBody></XyzBody>
    <XyzFooter></XyzFooter>
  </div>
</template>

<script>


import XyzHeader from "./components/xyz-header";
import XyzBody from "./components/xyz-body";
import XyzFooter from "./components/xyz-footer";
export default {
  name: 'app',
  components: {
    XyzFooter,
    XyzBody,
    XyzHeader

  }
}
</script>

<style>
#app {

}
</style>
