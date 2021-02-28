<template>
  <div class="button">
    <button class="button--component">{{ name }}</button>
  </div>
</template>

<script>
export default {
  props: {
    name: String
  },
  data() {
    return {

    }
  }
}
</script>

<style>
.button {
  padding: 20px;
}

.button--component {
  cursor: pointer;
}
</style>
