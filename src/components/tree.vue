<template id="item-template">
    <div>
        <div style="text-align:left">
            {{model.name}}
        </div>
        <!-- 组件中引用当前组件，传入下级数据 -->
        <div style="margin-left:20px">
            <tree class="tree" v-for="(model,index) in model.children" :key="index" :model="model"></tree>
        </div>
    </div>
</template>

<script>
export default {
  name: 'tree',
  template: '#item-template',
  props: {
        model: Object
  },
  data: function () {
      return {
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
