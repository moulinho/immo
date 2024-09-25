<template>
  <q-input
    v-model="modelValue"
    :label="label"
    :type="type"
    :required="required"
    :prepend-icon="prependIcon"
    outlined
    dense
  />
</template>

<script>
import { defineProps, defineEmits } from "vue";

const props = defineProps({
  modelValue: {
    type: String,
    required: true,
  },
  label: {
    type: String,
    required: true,
  },
  type: {
    type: String,
    default: "text",
  },
  prependIcon: {
    type: String,
    default: "",
  },
  required: {
    type: Boolean,
    default: false,
  },
});

const emit = defineEmits(["update:modelValue"]);

const updateValue = (value) => {
  emit("update:modelValue", value);
};
</script>
