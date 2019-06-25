<template>
    <div>
        <h1>Contact information</h1>

        <form-generator :schema="schema"
                        v-model="form">
        </form-generator>

        <p>
            {{form.phone}} {{form.email}} {{form.skype}} {{form.telegram}}
        </p>

    </div>
</template>

<script>
    import FormGenerator from '../components/v1/FormGenerator';

    export default {
        name: "ContactInformation",
        components: {FormGenerator},
        data() {
            return {
                form: {
                    phone: null,
                    email: null,
                    skype: '',
                    telegram: ''
                },
                schema: [
                    {
                        fieldType: "TelInput",
                        label: "Phone number: ",
                        name: "phone"
                    },
                    {
                        fieldType: "EmailInput",
                        label: "E-mail: ",
                        name: "email"
                    },
                    {
                        fieldType: "TextInput",
                        label: "Skype: ",
                        name: "skype"
                    },
                    {
                        fieldType: "TextInput",
                        label: "Telegram: ",
                        name: "telegram"
                    }
                ]
            };
        }
    }
</script>

<style scoped>

</style>