<template>
  <div class="row">
    <div class="col-sm-4">{{this.selected}}</div>
    <div class="col-sm-4">
    <q-select
      v-model="select"
      inverted-light
      color="grey-4"
      filter
      autofocus-filter
      filter-placeholder= "Search..."
      separator
      :display-value="displayvalue()"
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
      selected: [],
      select: '',
      selectOptions: [ { label: 'Option One', value: 'one' }, { label: 'Option Two', value: 'two' }, { label: 'Option Three', value: 'three' } ]
    }
  },
  watch: {
    select () {
      this.selected.push(this.select)
    }
  },
  methods: {
    displayvalue () {
      if (this.selected.length === 0) {
        return 'Select...'
      }
    }
  }
}
</script>
