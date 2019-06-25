<template>
    <div>
        <h1>General information</h1>

        <form-generator :schema="schema"
                        v-model="form">
        </form-generator>
        <br>
        <p>
            {{form.name}} {{form.surname}} {{form.patronymic}} {{form.birthday}}
        </p>
    </div>
</template>

<script>
    import FormGenerator from "../components/v1/FormGenerator";

    export default {
        name: "GeneralInformation",
        components: {FormGenerator},
        data() {
            return {
                form: {
                    name: 'Alina',
                    surname: '',
                    patronymic: '',
                    birthday: null
                },
                schema: [
                    {
                        fieldType: "TextInput",
                        label: "Name: ",
                        name: "name"
                    },
                    {
                        fieldType: "TextInput",
                        label: "Surname: ",
                        name: "surname"
                    },
                    {
                        fieldType: "TextInput",
                        label: "Patronymic: ",
                        name: "patronymic"
                    },
                    {
                        fieldType: "DateInput",
                        label: "Date of birth: ",
                        name: "birthday"
                    }
                ]
            };
        }
    };
</script>
