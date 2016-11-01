<template>
  <quasar-layout>
    <div slot="header" class="toolbar">
      <button class="hide-on-drawer-visible" @click="$refs.drawer.open()">
        <i>menu</i>
      </button>

      <quasar-toolbar-title :padding="1">
        Title
      </quasar-toolbar-title>
    </div>


    <quasar-drawer ref="drawer">
      <div class="toolbar">
        <quasar-toolbar-title>
          Drawer Title
        </quasar-toolbar-title>
      </div>

      <div class="list no-border platform-delimiter">
        <quasar-drawer-link icon="mail" to="/login" exact>
          Login
        </quasar-drawer-link>
        <quasar-drawer-link icon="mail" to="/hello" exact>
          Hello
        </quasar-drawer-link>
      </div>
    </quasar-drawer>


    <router-view class="layout-view"></router-view>

  </quasar-layout>
</template>

<script>
export default {
  data () {
    return {}
  }
}
</script>

<style>
</style>
