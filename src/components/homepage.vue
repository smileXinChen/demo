<template>
  <div id="homepage">
    <menu-head></menu-head>
    <con-left></con-left>
  </div>
</template>

<script>
import MenuHead from './hompage/head.vue'
import ConLeft from './hompage/conleft.vue'
export default {
  name:'homepage',
  data () {
    return {
    
    }
  },
  components:{
    MenuHead,
    ConLeft,
  }
}
</script>
<style scoped>
/* #homepage{
} */

</style>
