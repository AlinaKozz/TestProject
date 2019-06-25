<template>
  <div>
    <component v-for="(field, index) in schema"
               :key="index"
               :is="field.fieldType"
               :value="form[field.name]"
               @input="updateForm(field.name, $event)"
               v-bind="field">
    </component>
  </div>
</template>

<script>
import TextInput from "./TextInput";
import DateInput from "./DateInput";
import ButtonInput from "./ButtonInput";

export default {
  name: "FormGenerator",
  components: { TextInput, DateInput, ButtonInput },
  props: ["schema", "value"],
  data() {
    return {
      form: this.value || {}
    };
  },
  methods: {
    updateForm(fieldName, value) {
      this.$set(this.form, fieldName, value);
      this.$emit("input", this.form);
    }
  }
};
</script>
