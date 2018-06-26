<template>
  <q-page class="flex flex-center">
    <q-select
      v-model="select"
      float-label="Is Quasar Awesome?"
      radio
     :options="selectOptions"
    ><q-search v-model="searchModel"></q-search></q-select>
  </q-page>
</template>

<style>
</style>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      searchModel: '',
      select: 'fb',
      selectOptions: [
        {
          label: 'Google',
          value: 'goog'
        },
        {
          label: 'Facebook',
          value: 'fb'
        }
      ]
    }
  }
}
</script>
