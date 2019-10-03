<template>
<div>
<div class="pw-main"> 
  <div class="pw-header">
    <div class="pw-header-content">
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <img src="./assets/pickle-wiki-logo v9.png" class="pw-logo" />
    </div>
  </div>
  <div class="pw-content"></div>
  <div class="pw-footer"></div>
</div>


    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list class="pa-1">
        <v-list-tile avatar>
          <v-list-tile-avatar>
            <img src="https://randomuser.me/api/portraits/men/85.jpg">
          </v-list-tile-avatar>

          <v-list-tile-content>
            <v-list-tile-title>John Leider</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>

      <v-list class="pt-0" dense>
        <v-divider></v-divider>

        <v-list-tile
          v-for="item in items"
          :key="item.title"
          @click=""
        >
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>

          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>

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

.pw-header {
  width:100%;
  height:54px;
  background-color:#eaecf0;
  // box-shadow: 0 2px 3px #757575;
  box-shadow: 0px 2px 4px -1px rgba(0,0,0,0.2), 0px 4px 5px 0px rgba(0,0,0,0.14), 0px 1px 10px 0px rgba(0,0,0,0.12);
  position: absolute;
}

.pw-header-content {
  width:90%;
  margin-right: auto;
  margin-left: auto;
}

.pw-content {
  width:90%;
  height:550px;
  margin-right: auto;
  margin-left: auto;
  background-color:#FFF;  
}

.pw-footer {
  width:100%;
  height:100px;
  margin: 0;
  background-color:#eaecf0;
  border-top: solid 1px #c8ccd1;
  float: bottom;
}

.pw-logo {
  position: absolute;
  margin-top: 0.4%;
}
</style>

<script>
  export default {
    data () {
      return {
        drawer: null,
        items: [
          { title: 'Home', icon: 'dashboard' },
          { title: 'About', icon: 'question_answer' }
        ]
      }
    }
  }
</script>