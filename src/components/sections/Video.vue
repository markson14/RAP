<script setup>
const videos = [
  './videos/mp4_output/000_RD_Radio16_000__21s-10s.mp4',
  './videos/mp4_output/007_WDA_TomPerez_00_0s-13s.mp4',
  './videos/mp4_output/005_WDA_HaleySteven_10s-10s.mp4',
  './videos/mp4_output/014_WRA_PeterRoskam_0s-10s.mp4',
  './videos/mp4_output/004_RD_Radio8_000_c_0s-10s.mp4',
  './videos/mp4_output/008_WRA_AdamKinzing_0s-10s.mp4',
  './videos/mp4_output/001_RD_Radio1_000_c_0s-10s.mp4',
]
</script>

<template>
  <div class="video-section">
    <el-divider />
    <el-row justify="center">
      <h1 class="section-title">Qualitative Comparison</h1>
    </el-row>

    <el-row :gutter="20" justify="center">
      <el-col :xs="24" :sm="20" :md="16" :lg="10" :xl="10">
        asdf
      </el-col>
    </el-row>
    <!-- 视频网格展示 -->
    <el-row :gutter="20" justify="center">
      <el-row 
        v-for="(video, index) in videos" 
        :key="index"
        :xs="24" 
        :sm="20" 
        :md="16" 
        :lg="10" 
        :xl="10"
        class="video-col"
      >
        <div class="video-wrapper">
          <video 
            controls 
            preload="metadata" 
            playsinline
            class="video-player"
          >
            <source :src="video" type="video/mp4">
            Your browser does not support the video tag.
          </video>
        </div>
      </el-row>
    </el-row>
  </div>
</template>

<style scoped>
.video-section {
  padding: 20px 0;
  max-width: 100%;
  overflow-x: hidden;
}

.video-col {
  margin-bottom: 0px;
  display: flex;
  justify-content: center;
}

.video-wrapper {
  width: 1375px;
  max-width: auto;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  background: #f5f5f5;
}

.video-player {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 8px;
  max-height: 300px;
  object-fit: cover;
}

.section-title {
  margin-bottom: 30px;
  text-align: center;
  font-size: 2rem;
  font-weight: 600;
  color: #333;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .video-wrapper {
    max-width: 100%;
  }
  
  .section-title {
    font-size: 1.5rem;
    margin-bottom: 20px;
  }
}

@media (max-width: 480px) {
  .video-section {
    padding: 10px 0;
  }
  
  .section-title {
    font-size: 1.25rem;
    margin-bottom: 15px;
  }
}
</style>