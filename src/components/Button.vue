<template>
  <!-- dynamic values are captured with : -->
  <button :style="{ background: color }" class="btn" @click="onClick()">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: String,
    color: String,
  },
  methods: {
    onClick() {
      console.log("clicked");
    },
  },
};
</script>

<style></style>
