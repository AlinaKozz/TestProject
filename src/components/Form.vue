<template>
  <div>
    <h1>General information</h1>

    <form-generator :schema="schema"
                    v-model="form">
    </form-generator>

    
  </div>
</template>

<script>
import FormGenerator from "../components/v1/FormGenerator";

export default {
  name: "Form",
  components: { FormGenerator },
  data() {
    return {
      form: {
        name: "Alina"
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
        },
        {
          fieldType: "ButtonInput",
          label: "Ok",
          name: "button"
        }
      ]
    };
  }
};
</script>
