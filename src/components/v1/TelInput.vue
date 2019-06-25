<template>
    <div>
        <label>{{label}}</label>

        <input type="tel"
               :name="name"
               :value="value"
               @input="$emit('input',$event.target.value)">
    </div>
</template>

<script>
    export default {
        name: 'TelInput',
        props: ['label', 'name', 'value']
    }
</script>

<style scoped>

</style>