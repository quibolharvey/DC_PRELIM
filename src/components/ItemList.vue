<template>
  <div>
    <h1>Item List</h1>
    <div v-for="item in filteredItems" :key="item.id">
      <Item :item="item" @add-to-cart="handleAddToCart" />
    </div>
  </div>
</template>

<script>
import Item from './Item.vue';

export default {
  name: 'ItemList',
  components: {
    Item,
  },
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
  computed: {
    filteredItems() {
      return this.items.filter(item => item.visible);
    },
  },
  methods: {
    handleAddToCart(item) {
      console.log(`Added to cart: ${item.name}, Price: ${item.price}`);
    },
  },
};
</script>
