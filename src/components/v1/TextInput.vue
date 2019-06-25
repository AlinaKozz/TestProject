<template>
  <div>
    <label>{{label}}</label>

    <input type="text"
           :name="name"
           :value="value"
           @input="$emit('input',$event.target.value)">
  </div>
</template>

<script>
export default {
  name: 'TextInput',
  props: ['label', 'name', 'value']
}
</script>