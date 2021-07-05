<template>
  <div id="app">
    <div id="nav">
      <div id="title">Phsyical Therapy Tracker</div>
      <router-link to="/">Home</router-link> |
      <router-link to="/activities">Activities</router-link>
      <!-- <router-link to="/add">Add Activitiy</router-link> -->
    </div>
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 25px;
  display: block;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

#title {
  font-size: 14px;
  position: absolute;
  text-align: left;
  font-weight: bolder;
  font-style: italic;
}
</style>
