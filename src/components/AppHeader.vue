<script setup>
  import { ref } from 'vue'

  let isChange = ref(false)
  
  defineProps(['color'])

  const emit = defineEmits(['removeTodo'])

  // const closeRemove = (i) => emit('removeTodo', i)
  const closeRemove = function(i) {
    emit('removeTodo', i)
  }



</script>

<template>
  <header>
    <!-- <p v-on:click="add()">ボタン</p>
    <div v-bind:class="{ frame: isChange }">
      {{ message }}
    </div> -->
    <div class="inner">
      <h1><a href="/" :style="{ 'color': color }">Vue.js練習サイト</a></h1>
      <nav>
        <ul>
          <li id="pulldown" @click="closeRemove()">Nav1
          <!-- <li id="pulldown" @click="close(10)">Nav1 -->
            <ul>
              <li><a href="#">Child1</a></li>
              <li><a href="#">Child2</a></li>
              <li><a href="#">Child3</a></li>
            </ul>
          </li>
          <li><a href="#Nav2">Nav2</a></li>
          <li><a href="#Nav3">Nav3</a></li>
          <li><a href="#Nav4">Nav4</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>