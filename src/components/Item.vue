<template>
  <div v-if="item.isVisible">
    <h2>{{ item.name }}</h2>
    <p>Price: {{ item.price }}</p>
    <button @click="addToCart">Add to Cart</button>
  </div>
</template>

<script>
export default {
  name: 'Item',
  props: {
    item: {
      type: Object,
      required: true,
    },
  },
  methods: {
    addToCart() {
      this.$emit('add-to-cart', this.item);
    },
  },
};
</script>
