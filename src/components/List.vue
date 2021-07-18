<template>
  <div>
    <Item
      v-for="[k, v] of fields"
      :key="k"
      :value="v"
      :name="k"
      @input="$emit('input', { ...value, [k]: $event })"
    />
  </div>
</template>

<script>
import Item from "./Item";

export default {
  components: { Item },
  props: {
    value: {},
  },
  computed: {
    fields() {
      return Object.entries(this.value);
    },
  },
};
</script>

<style></style>
