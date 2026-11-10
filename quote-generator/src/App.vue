<template>
    <div id="app" class="container">
    <h1>Home</h1>

    <div id="nav">
      <router-link to="/about">About</router-link>
      <br>
      <router-link to="/contact">Contact</router-link>
      <br>
      <router-link to="/quotes">Quotes</router-link>
    </div>

    
   

    <div class="container">
      <router-view></router-view>
    </div>

    
  </div>
</template>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.container {
  text-align: center;
  font-family: Arial, sans-serif;
  margin-top: 50px;
}
button {
  margin-top: 20px;
  padding: 10px 20px;
  font-size: 16px;
}
.author {
  font-style: italic;
  color: #555;
  margin-top: 5px;
}
</style>
