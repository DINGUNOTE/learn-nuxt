<template>
  <div class="input-wrapper flex">
    <input
      type="text"
      class="text-input"
      :value="value"
      @input="$emit('input', $event.target.value)"
    />
    <button type="button" class="btn" @click="$emit('search')">search</button>
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: String,
      default: () => '',
    },
  },
};
</script>

<style scoped>
.input-wrapper {
  margin: 1rem 0;
  height: 40px;
}
.search-input {
  width: 200px;
  font-size: 1.2rem;
  font-weight: 500;
}
.btn {
  font-size: 1.2rem;
  font-weight: 500;
}
</style>
