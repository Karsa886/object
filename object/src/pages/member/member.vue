<template>
  <div>

    <!-- 列表 -->
    <v-list @edit="edit"></v-list>
  </div>
</template>
<script>
import vList from "./components/list";
export default {
  components: {
    vList,
  },
  data() {
    return {
              info: {
        //弹框的出现状态
        show: false,
        title:"分类添加",
        isAdd:true
      },
    };
  },
  methods: {

    //点击了编辑
    edit(id){
        this.info.show=true;
         this.info.title="会员编辑"
         this.info.isAdd=false
        this.$refs.add.getDetail(id)
    }
  },
  mounted() {},
};
</script>
<style scoped>
</style>