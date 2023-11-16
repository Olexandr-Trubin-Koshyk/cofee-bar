<template>
  <input
    :type="type"
    :placeholder="placeholder"
    v-model="inputValue"
    class="input"
    :class="{ 'input--error': isInputError, 'input--success': isInputSuccess }"
  />
</template>

<script lang="ts">
import { PropType } from "vue";
import { defineComponent } from "vue";
import InputType from "@/types/InputType";
import { ref } from "vue";

export default defineComponent({
  props: {
    type: {
      required: true,
      type: String as PropType<InputType>,
    },
    placeholder: {
      required: true,
      type: String,
    },
  },
  setup() {
    const inputValue = ref<string>("");
    const isInputError = ref<boolean>(false);
    const isInputSuccess = ref<boolean>(false);

    return { inputValue, isInputError, isInputSuccess };
  },
});
</script>

<style lang="scss" scoped>
@import "../styles/main.scss";
.input {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 150%;
  padding-bottom: 4px;
  padding-left: 8px;
  color: $color-grey;
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
  transition: border-bottom 0.3s ease-in;

  &:focus {
    border-bottom: 1px solid $color-marine-blue;
  }

  &--error,
  &--error:focus {
    color: $color-flamingo-error;
    border-bottom: 1px solid $color-flamingo-error;

    &::placeholder {
      color: $color-flamingo-error;
    }
  }

  &--success,
  &--success:focus {
    color: $color-marine-blue;
    border-bottom: 1px solid $color-marine-blue;

    &::placeholder {
      color: $color-marine-blue;
    }
  }
}
</style>
