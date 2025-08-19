<script setup>
import page from "../mds/md.mdx";
</script>

<template>
  <el-divider />
  <el-row justify="center">
    <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
      <page />
    </el-col>
  </el-row>
  <div style="display: flex; justify-content: center; margin-bottom: 24px">
    <el-col :xs="24" :sm="20" :md="16" :lg="10" :xl="10">
      <el-image
        src="./模型图_0802_1830.png"
        style="
          width: 100%;
          height: auto;
          border-radius: 12px;
          box-shadow: 0 2px 12px rgba(0, 0, 0, 0.08);
        "
        fit="contain"
      />
    </el-col>
  </div>
</template>
