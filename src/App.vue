<script>
import Navbar from "./components/layout/Navbar.vue";
export default {
  components: {
    Navbar
  },
  methods:{
    check_loading(){
      let timer = setInterval(() => {
        if(document.readyState === "complete"){
          clearInterval(timer);

        }
      },300)
    }
  },
  mounted(){
    this.check_loading();
  }
}
</script>

<template>
  <Navbar></Navbar>
    <main class="page-content">
      <RouterView />
      <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br> <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br> <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br> <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
    </main>
</template>

<style scoped>

</style>
