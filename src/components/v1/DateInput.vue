<template>
  <div>
    <label>{{label}}</label>

    <input type="date"
           :name="name"
           :value="value"
           @input="$emit('input',$event.target.value)">
  </div>
</template>

<script>
export default {
  name: 'DateInput',
  props: ['label', 'name', 'value']
}
</script>