<template>
<div id="pw-main"> 
  <div id="pw-header">
    <div id="pw-header-content">
      <v-toolbar-side-icon></v-toolbar-side-icon>
    </div>
  </div>
  <div id="pw-content"></div>
  <div id="pw-footer"></div>
</div>
</template>

<style lang="scss">
#pw-main {
  width:100%;
  margin-top:0;
  margin-left:auto;
  margin-bottom:0;
  margin-right:auto;
  background-color:#666;
}

#pw-header {
  width:100%;
  height:54px;
  background-color:#eaecf0;
  box-shadow: inset 0 -1px 3px rgba(0,0,0,0.08);
  float: bottom;
}

#pw-header-content {
  width:90%;
  margin-right: auto;
  margin-left: auto;
}

#pw-content {
  width:90%;
  height:550px;
  margin-right: auto;
  margin-left: auto;
  background-color:#FFF;  
}

#pw-footer {
  width:100%;
  height:100px;
  margin: 0;
  background-color:#eaecf0;
  border-top: solid 1px #c8ccd1;
  float: bottom;
}

</style>
