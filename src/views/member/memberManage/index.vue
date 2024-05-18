<template>
    
<div class="container" style="margin-left: 20px;">
     <div class="Main">
        <div class="range">
          <el-card class="box-card">
              <p>知识库公开范围</p>
              <el-radio v-model="radio" label="1">仅当前知识库成员可见</el-radio>
              <br>
              <el-radio v-model="radio" label="2">{{ name.name }}所有人和知识库成员可见</el-radio>
          </el-card>
      </div>
<span>角色与权限</span>
  <i class="el-icon-question" style="margin-left: 4px;"></i>
  <br>
      <div class="manage">
        
          <div>
        
              <el-menu :default-active="activeIndex2" class="el-menu-demo" mode="horizontal" @select="handleSelect">
              <el-menu-item index="1">管理员</el-menu-item>
              <el-menu-item index="2">可编辑的成员</el-menu-item>
              <el-menu-item index="3">可阅读的成员</el-menu-item>

              <el-input
                placeholder="搜索已有内容"
                prefix-icon="el-icon-search"
                v-model="input2" style="border-radius: 20px;"
              ></el-input>
              </el-menu>

            </div>

          <div class="add">

              <div>页面默认权限：可编辑</div> 
              <button class="Add"><i class="el-icon-plus"></i>添加成员</button>

          </div>

          <el-divider></el-divider>

      </div>


    </div>
  
</div>
</template>
<script>
import { getDefaultState } from '@/store/modules/user.js'

export default {
  
  data() {
    return {
      // activeIndex: '2',
      activeIndex2: '2',
      name:{}
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  },
  created(){
          this.name = getDefaultState();
  }
}

</script>
<style>

.nav{
  
  margin-top: 0px;
}
.range{
  
  margin-top: 50px;
  
  margin-bottom: 50px;
  /* border: solid 1px rgb(179, 167, 167); */
  border-radius: 5px;
}

.Main{
  width: 85%;
}
/* .manage{
 
  display: flex;
} */
.el-input{
 
 /* margin-left: 450px; */
 position: absolute;
 right: 0;
  
  width: 300px;
}
.el-tabs{
  flex-grow:1;
}

.add{
  height: 80px;
  display: flex;
  align-items: center;
}
.el-divider{
  margin-top: 0px;
}
.add div{
  flex-grow: 1;
}
.Add{
      width: 110px;
      height: 35px;
      border-radius: 10px;
      border: solid 1px rgb(59, 76, 232);
      background-color: white;
      color:rgb(59, 76, 232) ;

}
</style>