<template>
<div>
<div class="pw-main"> 
  <pw-header></pw-header>
  <pw-content></pw-content>
  <pw-footer></pw-footer>
  <pw-drawer></pw-drawer>
</div>

</div>
</template>

<style lang="scss">
.pw-main {
  width:100%;
  margin-top:0;
  margin-left:auto;
  margin-bottom:0;
  margin-right:auto;
  background-color:#666;
}
</style>

<script>
  export default {
    components: {
      'pw-header': () => import('./components/Header'),
      'pw-drawer': () => import('./components/Drawer'),
      'pw-content': () => import('./components/Content'),
      'pw-footer': () => import('./components/Footer'),
    },
    data () {
      return { }
    }
  }
</script>