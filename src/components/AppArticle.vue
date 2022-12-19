

<!-- 参考サイト https://summershiro.com/2022/10/10/slider/ -->
<script setup>
import { ref } from 'vue'
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

const slideImagesArr = ref([
  'https://placehold.jp/500x300.png?text=1',
  'https://placehold.jp/500x300.png?text=2',
  'https://placehold.jp/500x300.png?text=3',
])

const articlesImagesArr = ref([
  {
    url: "https://www.google.com/",
    image: 'https://placehold.jp/500x300.png?text=tmb1',
    title: 'タイトル1タイトル1',
    text: 'テキスト1テキスト1テキスト1'
  },
  {
    url: "https://www.google.com/",
    image: 'https://placehold.jp/500x300.png?text=tmb2',
    title: 'タイトル2タイトル2',
    text: 'テキスト2テキスト2テキスト2'
  },
  {
    url: "https://www.google.com/",
    image: 'https://placehold.jp/500x300.png?text=tmb3',
    title: 'タイトル3タイトル3',
    text: 'テキスト3テキスト3テキスト3'
  },
  {
    url: "https://www.google.com/",
    image: 'https://placehold.jp/500x300.png?text=tmb4',
    title: 'タイトル4タイトル4',
    text: 'テキスト4テキスト4テキスト4'
  },
])
</script>

<template>
  <div class="contain">
    <carousel :items-to-show="1">
      <slide v-for="slide in slideImagesArr" :key="slide">
        <img :src="slide">
      </slide>

      <template #addons>
        <navigation />
        <pagination />
      </template>
    </carousel>
    
    <div class="articles">
      <ul>
        <li v-for="article in articlesImagesArr">
          <a :href="article.url"><img :src="article.image"><h3>{{ article.title }}</h3><p>{{ article.text }}</p></a>
        </li>
      </ul>
    </div>
  </div>
</template>




