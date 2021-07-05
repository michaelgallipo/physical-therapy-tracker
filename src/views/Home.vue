<template>
  <div class="home">
    <img id="logo" alt="Frankie the Ferret" src="../assets/MLH-Mascots.png" />
    <img id="splash" alt="leg extension machine" src="../assets/Splash.jpg" />
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home"
  // components: {
  //   HelloWorld
  // }
};
</script>

<style>
#logo {
  height: 150px;
  width: 150px;
}

#splash {
  width: 90vw;
  margin-top: 20px;
}
</style>
