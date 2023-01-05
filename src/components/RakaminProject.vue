<template>
  <div id="app">
    <header>
      <slot name="header" />
      <p>Dreamer | Learner</p>
    </header>
    <h1>{{ title }}</h1>
    <button @click="title = 'Mufid Rakamin Project'">BUTTON</button>
    
    <h3>Favorite Menu</h3>
    <al>
      <li v-for="item in drink" :key="item.name">
        {{ item.name }} - {{ item.price }}
      </li>
    </al>
    <h5>Select Tag</h5>
    <select>
      <option>Select</option>
      <option>Mineral Water</option>
      <option>Fried Rice</option>
      <option>Milk</option>
      <option>Coffee</option>
      <option>Tea</option>
    </select>
    <h5>Text Area</h5>
    <textarea rows="4" cols="50"></textarea>
     
    <footer >
      <slot name="footer" />
      <p>The Mufid 2022. All Right Reserved</p>
    </footer>
  </div>
</template>
 
<script>
export default {
  name: "App",
  props: {},
  data() {
    return {
      title: "Mufid Rakamin Project",
      drink: [
        { name: "Mineral Water", price: 30.000 },
        { name: "Fried Rice", price: 25.000 },
        { name: "Milk", price: 20.000 },
        { name: "Coffee", price: 15.000 },
        { name: "Tea", price: 10.000 },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
