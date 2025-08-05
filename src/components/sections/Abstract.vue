<script setup>
import abstract from '../mds/abstract.mdx';
</script>

<template>
  <div>
    <div style="display: flex; justify-content: center; margin-bottom: 24px;">
      <el-image
        src="./head_image_v3.png"
        style="max-width: 60vw; width: 1315px; height: auto; border-radius: 12px; box-shadow: 0 2px 12px rgba(0,0,0,0.08);"
        fit="contain"
      />
    </div>
    <el-row justify="center">
      <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
        <abstract />
      </el-col>
    </el-row>
  </div>
</template>