<script>
import Title from "./sections/Title.vue";
import Abstract from "./sections/Abstract.vue";
import Markdown from "./sections/Markdown.vue";
import BibTeX from "./sections/BibTeX.vue";
import Carousel from "./sections/Carousel_linguish.vue";
import Carousel_3d from "./sections/Carousel_3d.vue";

export default {
  components: {
    Title,
    Abstract,
    Markdown,
    Carousel,
    Carousel_3d,
    BibTeX,
  },
};
</script>

<template>
  <Title />
  <Abstract />
  <Markdown />
  <Carousel />
  <Carousel_3d />
  <BibTeX />
</template>
