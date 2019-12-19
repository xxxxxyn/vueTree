<template>
  <ul>
    <li v-for="item in treeData" :key='item.text'>
      <input type="button" v-if="item.children" @click="openList()" v-model="openText">
      {{item.text}}
      <tree :treeData="item.children" v-if="isShow"></tree>
    </li>
  </ul>

</template>

<script>


  export default {
    name: "tree",
    props: {
      treeData: {
        default: function () {
          return []
        }
      },

    },
    data() {
      return {
        isShow: false,
        openText:'展开'
      }
    },
    methods: {
      openList() {
        this.isShow = !this.isShow
        if(this.isShow!==false){
          this.openText='关闭'
        }else{
          this.openText='展开'
        }

      }

    }
  }
</script>

<style scoped>
*{
  list-style: none;
}
</style>
