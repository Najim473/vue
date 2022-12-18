<template>
  <div class="main">
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatem in
      vero ex esse error ducimus, facere omnis tempora obcaecati officiis!
    </p>
    <compo name="Mango" name2="Apple"/>
    <compo name="Apple" name2="Mango"/>
    <compo name="Banana" name2="Apple"/>
    <compo :name="name" :name2="name2"/>
  </div>
</template>
 <script>
 import compo from './component.vue'
export default{
  name:'myHome',
 components:{
  compo
 },
 data(){
  return{
    name: 'Lemon',
    name2:'Orange'
  }
 }
}
</script>
<!-- <style lang="scss" scoped>
@import "./myHome.scss";
</style> -->
