<template>
   <div class="text-input" ref="input">
      <label :for="id">{{ placeholder }}</label>

      <input
         type="text"
         :id="id"
         @input="emit('update:modelValue', $event?.target?.value)"
         :value="props.modelValue"
         v-maska
         data-maska="+7 (###) ###-##-##"
         v-if="isPhone"
      />
      <input
         type="text"
         :id="id"
         @input="emit('update:modelValue', $event?.target?.value)"
         :value="props.modelValue"
         v-else
      />
   </div>
</template>
<script setup>
const emit = defineEmits(["update:modelValue"]);
let props = defineProps({
   id: String,
   modelValue: String,
   placeholder: String,
   isPhone: {
      type: Boolean,
      default: false,
   },
   isEmail: {
      type: Boolean,
      default: false,
   },
});
let input = ref(null);

function watchForValue(value) {
   if (value) {
      input?.value?.classList.add("filled");
      input?.value?.classList.remove("error");
   } else {
      input?.value?.classList.remove("filled");
   }
}
onMounted(() => {
   watchForValue(props.modelValue);
});
watch(
   () => props.modelValue,
   (value) => {
      watchForValue(value);
   }
);
</script>
