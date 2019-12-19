<template>
  <div id="app">
    <tree :treeData="treeData"></tree>
  </div>
</template>

<script>
  import tree from './components/tree'

  let treeData = [
    {
      text: "一级-1",
      children: [
        {
          text: "二级-1",
        },
        {
          text: "二级-2",
          children: [
            {
              text: "三级-1",
            },
            {
              text: "三级-2",
            }
          ]
        }
      ]
    },
    {
      text: "一级-2",
    }
  ];

  export default {
    name: 'app',
    components: {
      tree
    },
    data(){
      return {
        treeData
      }
    }
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
