<script>
import { Swiper, SwiperSlide} from 'swiper/vue';
import { Navigation, Pagination, Autoplay} from 'swiper/modules';
import 'swiper/css/bundle';

export default {
  components: {
      Swiper,
      SwiperSlide,
      Navigation,
      Pagination,
      Autoplay,
    },
  data() {
    return {
      modules: [
        Navigation,
        Pagination,
        Autoplay,
      ],
      // 选择要轮播的视频
      video_paths: [
        "./videos/20250805-100055.957-0.mp4",
        "./videos/20250805-100055.957-1.mp4",
        "./videos/20250805-100055.957-2.mp4",
        "./videos/20250805-100055.957-3.mp4",
      ],
    }
  }
}
</script>

<template>
  <el-divider />
  <h1>Demo</h1>
  <el-row justify="center">
    <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
      <!-- 设置轮播图：循环播放、首张图序号、响应式、导航和分页、自动播放 -->
      <swiper
        :loop="true"
        :slidesPerView="1"
        :breakpoints="{
          600: {
            slidesPerView: 3,
          },
          800: {
            slidesPerView: 4,
          },
        }"
        :modules="modules"
        :navigation="{ 
          hideOnClick:true,
        }"
        :pagination="{ 
          hideOnClick:true,
          clickable:true, 
          type:'bullets' 
        }"
        :autoplay="{ 
          delay:5000,
          disableOnInteraction:false,
          pauseOnMouseEnter:true,
        }"
        >
        <swiper-slide v-for="path in video_paths" :key="path">
          <div class="video-container">
            <video 
              :src="path" 
              controls
              preload="metadata"
              class="carousel-video"
            >
              您的浏览器不支持视频播放。
            </video>
          </div>
        </swiper-slide>
      </swiper>
    </el-col>
  </el-row>
</template>
  
<style>

/* 设置Swiper风格 */
.swiper {
  --swiper-theme-color: white;
}

/* 视频容器样式 */
.video-container {
  width: auto;
  height: auto;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 10px;
}

/* 视频样式 */
.carousel-video {
  width: auto;
  height: 100%;
  object-fit: contain;
  border-radius: 8px;
  max-width: 100%;
  max-height: 100%;
}

/* 响应式调整 */
@media (max-width: 768px) {
  .video-container {
    height: 600px;
  }
}

@media (max-width: 480px) {
  .video-container {
    height: 500px;
  }
}

</style>
  