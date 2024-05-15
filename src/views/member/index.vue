<template>
  <div class="member-container">
    <div class="navigaition">
      <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
        <el-menu-item index="1">基本信息</el-menu-item>
        <el-menu-item index="2">成员设置</el-menu-item>
        <el-menu-item index="3">安全设置</el-menu-item>
        <el-menu-item index="4">更多</el-menu-item>
      </el-menu>
    </div>
    <basic-info></basic-info>
    <member-manage></member-manage>
    <member-information></member-information>
    <more></more>
  </div>
</template>
<script>
import memberManage from '@/views/member/memberManage/index.vue'
import memberInformation from '@/views/member/memberInformation/index.vue'
import basicInfo from '@/views/member/basicInfo/index.vue'
import more from '@/views/member/more/index.vue'

export default {
  components: {
    memberManage,
    memberInformation,
    basicInfo,
    more
  }
}
</script>
<style scoped>

</style>
