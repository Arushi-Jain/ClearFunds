<template>
  <div class="flex flex-center">
    <q-select
      v-model="select"
      float-label="Is Quasar Awesome?"
     :options="selectOptions"
    ><q-search v-model="searchModel"></q-search></q-select>
  </div>
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
