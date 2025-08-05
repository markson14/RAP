<script setup>
import page from '../mds/md.mdx';
</script>

<template>
    <el-divider />
    <el-row justify="center">
        <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
            <page />
        </el-col>
    </el-row>
    <div style="display: flex; justify-content: center; margin-bottom: 24px;">
        <el-image 
            src="./模型图_0802_1830.png" 
            style="max-width: 60vw; width: 1375px; height: auto; border-radius: 12px; box-shadow: 0 2px 12px rgba(0,0,0,0.08);"
            fit="contain"
        />
    </div>
</template>