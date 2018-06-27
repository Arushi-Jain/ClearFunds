<template>
  <div class="row">
    <div class="col-sm-4"></div>
    <div class="col-sm-4">
    <q-select
      v-model="select"
      inverted-light
      color="grey-4"
      filter="true"
      autofocus-filter="true"
      filter-placeholder= "Search"
      separator
      display-value="Select..."
      static-label="Is Quasar Awesome?"
     :options="selectOptions"
    ></q-select>
    </div>
  </div>
</template>

<style>
</style>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      selectOptions: [ { label: 'Option One', value: 'one' }, { label: 'Option Two', value: 'two' }, { label: 'Option Three', value: 'three' } ]
    }
  }
}
</script>
