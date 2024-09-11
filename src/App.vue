<template>
  <div id="app">
    <ItemList :items="products" />
  </div>
</template>

<script>
import ItemList from './components/ItemList.vue';

export default {
  name: 'App',
  components: {
    ItemList,
  },
  data() {
    return {
      products: [
        { id: 1, name: 'DUMBELL', price: 100, isVisible: true, visible: true },
        { id: 2, name: 'BAR', price: 200, isVisible: true, visible: true },
        { id: 3, name: 'BARBELL', price: 300, isVisible: true, visible: true },
        { id: 4, name: 'BELT', price: 400, isVisible: true, visible: true },
        { id: 5, name: 'STRAP', price: 500, isVisible: true, visible: true },
      ],
    };
  },
};
</script>
<style>
button{
  width: 100px;
  height: 30px;
  border-radius: 10px;
}
button:hover{
  background-color: gray;
  justify-content: center;
}
</style>
