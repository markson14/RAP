<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Markdown from './sections/Markdown.vue'
import BibTeX from './sections/BibTeX.vue'
import Carousel from './sections/Carousel_linguish.vue'
import Carousel_sing from './sections/Carousel_sing.vue'
import Carousel_long from './sections/Carousel_long.vue'
import Video from './sections/Video.vue'

export default {
  components: {
    Title,
    Abstract,
    Markdown,
    Carousel,
    // Carousel_sing,
    // Carousel_long,
    // BibTeX,
    // Video,
  }
}
</script>

<template>
  <Title/>
  <Abstract/>
  <Markdown/>
  <Carousel/>
  <Carousel_long/>
  <Carousel_sing/>
  <Video/>
  <Latex/>
  <Table/>
  <Collapse/>
  <Echart/>
  <Model3D/>
  <GaussianSplats3D/>
  <SeletionForComparison/>
  <ImageSliderInner/>
  <ImageSlider/>
  <ImageSelector/>
  <BibTeX/>
  <Comment/>
</template>