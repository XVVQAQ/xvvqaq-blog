<template>
<nav class="navContainer" :class=[navState]>
  <RouterLink to="/">
    XVVQAQ's Blog
  </RouterLink>
  <div>
    <RouterLink to="/home">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
    <RouterLink to="/archive">Archive</RouterLink>
  </div>
</nav>
</template>

<script>
export default {
  data(){
    return {
      top:0,
      navState:{

      }
    }
  },
  mounted() {
    window.addEventListener('scroll', ()=>{
      this.top=document.body.scrollTop||
          document.documentElement.scrollTop||
          window.pageYOffset;
    });
  },
/*  watch: {
    top(newVal,oldVal){
      if(newVal===0){
        this.navState=["Top"]
      }else if(newVal>oldVal){
        //不知道什么更高级的语法了,干脆直接ififif
        if(newVal<500){
          this.navState=["noPin"]
        }else {
          this.navState=["navHidden"]
        }
      }else if(oldVal>newVal){
        this.navState=[""]
      }
    }
  }*/
}
</script>

<style scoped>
/*.navContainer{
  position: fixed;
  display: flex;
  top: 0;
  left: 0;
  right: 0;
  width: 100%;
  transform: translateY(0%);
  visibility: visible;
  transition: visibility 0.5s ease,transform 0.5s ease,background-color 0.5s ease;
}
.Top{
  height:50px;
  backdrop-filter: blur(0px);
  transition: height 0.5s ease,backdrop-filter 0.5s ease;
}
.navHidden{
  transform: translateY(-100%);
  opacity: 0;
  visibility: hidden;
  transition: visibility 0.5s ease,opacity 0.5s ease,transform 0.5s ease;
}
.noPin{
  height:50px;
  background-color: orange;
  backdrop-filter: blur(10px);
  transition: height 0.5s ease,backdrop-filter 0.5s ease,background-color 0.5s ease;
}
*/
</style>