
<template>
  <div class="app-container">
<!--    <set-navigation />-->
    <div class="allowShare">
      <p>是否允许页面被分享到组织外？</p>
      <br><br>
      <el-radio v-model="radio" label="1">允许</el-radio>
      <br><br>
      <el-radio v-model="radio" label="2">不允许</el-radio>
    </div>
    <div class="whoBuilt">
      <p>谁可以新建知识库的一级页面？</p>
      <br><br>
      <el-radio v-model="radio2" label="1">管理员和成员</el-radio>
      <br><br>
      <el-radio v-model="radio2" label="2">仅管理员</el-radio>
    </div>
    <div class="whoSeebase">
      <p>谁可以看到知识库设置中的基本信息？</p>
      <br><br>
      <el-radio v-model="radio3" label="1">可访问知识库的组织内用户和知识库成员中的关联组织成员</el-radio>
      <br><br>
      <el-radio v-model="radio3" label="2">仅知识库成员（包括关联组织成员）</el-radio>
    </div>
    <div class="allowCopy">
      <p>是否允许可阅读的用户对知识库内的页面内容进行复制，创建副本，打印，或导出（Word，PDF，图片等）？</p>
      <br><br>
      <el-radio v-model="radio4" label="1">允许</el-radio>
      <br><br>
      <el-radio v-model="radio4" label="2">不允许</el-radio>
    </div>
    <div class="allowComment">
      <p>是否允许可阅读的用户在页面进行评论？</p>
      <br><br>
      <el-radio v-model="radio5" label="1">允许</el-radio>
      <br><br>
      <el-radio v-model="radio5" label="2">不允许</el-radio>
    </div>
    <div class="whoMove">
      <p>谁可以移动或删除知识库的子页面</p>
      <br><br>
      <el-radio v-model="radio6" label="1">拥有子页面可管理权限的协作者</el-radio>
      <br><br>
      <el-radio v-model="radio6" label="2">同时拥有子页面可管理权限以及父页面可编辑权限的作者</el-radio>
    </div>

  </div>

</template>
<script>
// import setNavigation from '@/components/setnavigation/index.vue'
export default {

  // components: {
  //   setNavigation
  // },
  data() {
    return {
      radio: '1',
      radio2: '1',
      radio3: '1',
      radio4: '1',
      radio5: '1',
      radio6: '1',
      activeIndex: '1',
      activeIndex2: '1'
    }
  },

  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>
<style>
 /* .allowShare{
    padding-left: 20px;
    padding-top: 20px;
    padding-bottom: 20px;
    box-shadow:2px 5px 10px 1px rgb(25, 25, 25);
    border-radius: 20px;

} */

</style>
