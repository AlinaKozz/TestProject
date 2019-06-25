<template>
    <div>
        <h1>Education</h1>

        <form-generator :schema="schema"
                        v-model="form">
        </form-generator>

        <p>
            {{form.university}} {{form.faculty}} {{form.specialty}} {{form.graduated}}
        </p>

    </div>
</template>

<script>
    import FormGenerator from "../components/v1/FormGenerator";

    export default {
        name: "Education",
        components: {FormGenerator},
        data() {
            return {
                form: {
                    university: '',
                    faculty: '',
                    specialty: '',
                    graduated: null
                },
                schema: [
                    {
                        fieldType: "TextInput",
                        label: "University: ",
                        name: "university"
                    },
                    {
                        fieldType: "TextInput",
                        label: "Faculty: ",
                        name: "faculty"
                    },
                    {
                        fieldType: "TextInput",
                        label: "Specialty: ",
                        name: "specialty"
                    },
                    {
                        fieldType: "MonthInput",
                        label: "Graduated: ",
                        name: "graduated"
                    }
                ]
            };
        }
    }
</script>

<style scoped>

</style>