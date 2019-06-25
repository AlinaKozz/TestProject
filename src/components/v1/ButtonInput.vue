<template>
    <div>
        <label>{{label}}</label>

        <input type="submit"
               :name="name"
               :value="value"
               @input="$emit('input',$event.target.value)">
    </div>
</template>

<script>
    export default {
        name: 'ButtonInput',
        props: ['label', 'name', 'value']
    }
</script>