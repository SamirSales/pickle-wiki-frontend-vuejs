<template>
    <div class="pw-header">
    <div class="pw-header-content">
      <v-toolbar-side-icon @click.stop="openOrCloseDrawer()"></v-toolbar-side-icon>
      <img src="../assets/pickle-wiki-logo v9.png" class="pw-logo" />
    </div>
  </div>
</template>

<style scoped>
.pw-header {
  width:100%;
  height:54px;
  background-color:#eaecf0;
  box-shadow: 0px 2px 4px -1px rgba(0,0,0,0.2), 0px 4px 5px 0px rgba(0,0,0,0.14), 0px 1px 10px 0px rgba(0,0,0,0.12);
  position: absolute;
}

.pw-header-content {
  width:90%;
  margin-right: auto;
  margin-left: auto;
}

.pw-logo {
  position: absolute;
  margin-top: 0.4%;
}
</style>

<script>
import EventBus from '../eventBus.js';

export default {
    data: () => ({
        isDrawerOpened: false
    }),
    methods: {
        openOrCloseDrawer() {
            EventBus.$emit('openOrCloseDrawer', !this.isDrawerOpened);
        }
    }
}
</script>