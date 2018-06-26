<template>
    <q-layout view="hHr LpR lFf">
   <q-layout-header>
    <q-toolbar color="secondary">
      <q-btn
        flat round dense
        icon="menu"
        @click="left = !left"
        aria-label="Toggle menu on left side"
      />
      <q-toolbar-title>
        {{ $t(this.$store.state.views.title) }}
      </q-toolbar-title>
    </q-toolbar>
     <q-layout-drawer
      side="left"
      v-model="left"
      :behavior="behavior"
      :content-class="$q.theme === 'mat' ? 'bg-grey-3' : null"
    >
      <q-scroll-area class="fit">
        <q-list-header>
          <q-icon name="person" size="80pt" class="justify-center"/>
         </q-list-header>
        <q-item to="/profile">
          <q-item-side icon="account circle" />
          <q-item-main :label= "$t('user')" />
          <!-- <q-item-side right icon="thumb_up" /> -->
        </q-item>
        <q-item to="/home">
          <q-item-side icon="home" />
          <q-item-main :label= "$t('home')" />
        </q-item>
        <q-item to="/plan">
          <q-item-side icon="chrome_reader_mode" />
          <q-item-main :label= "$t('plan')" />
        </q-item>
        <q-item to="/loanapp">
          <q-item-side icon="assignment" />
          <q-item-main :label= "$t('loan')" />
        </q-item>
        <q-item to="/settings">
          <q-item-side icon="settings" />
          <q-item-main :label= "$t('settings')" />
        </q-item>
        <q-item to="/login">
          <q-item-side icon="power_settings_new" />
          <q-item-main :label= "$t('logout')" />
        </q-item>
         <q-item to="/about">
          <q-item-side icon="info" />
          <q-item-main :label= "$t('about')" />
        </q-item>
      </q-scroll-area>
    </q-layout-drawer>
  </q-layout-header>
  <q-page-container>
    <router-view/>
  </q-page-container>
</q-layout>
</template>

<script>

export default {
  data () {
    return {
      left :false,
      behavior: 'default'
    }
  }
}
</script>

<style>
</style>
