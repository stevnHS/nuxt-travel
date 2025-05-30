<script setup lang="ts">
const colorMode = useColorMode();

const isDark = computed({
  get: () => colorMode.preference === "dark",
  set: (value: boolean) => {
    colorMode.preference = value ? "dark" : "light";
  },
});
</script>

<template>
  <label class="swap swap-rotate mx-4">
    <input v-model="isDark" type="checkbox">
    <Icon
      name="tabler:sun"
      class="swap-on h-10 w-10 fill-current"
      size="24"
    />
    <Icon
      name="tabler:moon-filled"
      class="swap-off h-10 w-10 fill-current"
      size="24"
    />
  </label>
</template>
