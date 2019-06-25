<template>
    <div>
        <label>{{label}}</label>

        <input type="month"
               :name="name"
               :value="value"
               @input="$emit('input',$event.target.value)">
    </div>
</template>

<script>
    export default {
        name: 'MonthInput',
        props: ['label', 'name', 'value']
    }
</script>