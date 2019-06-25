<template>
    <div>
        <label>{{label}}</label>

        <input type="email"
               :name="name"
               :value="value"
               @input="$emit('input',$event.target.value)">
    </div>
</template>

<script>
    export default {
        name: 'EmailInput',
        props: ['label', 'name', 'value']
    }
</script>

<style scoped>

</style>