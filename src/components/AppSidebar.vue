<script setup>
  import { ref } from 'vue'

  const arrImage1 = ref(['a', 'b', 'c'])
  const arrLink1 = ref(['aa', 'bb', 'cc'])

  const arrImage2 = ref(['d', 'e', 'f'])
  const arrLink2 = ref(['dd', 'ee', 'ff'])

</script>

<template>
  <div class="sidebar">
    <div class="wrap">
      <h3>注目ラインナップ</h3>
      <nav>
        <ul>
          <li v-for="(ar, i) in arrImage1"><a :href="'/' + arrLink1[i] + '/'"><img :src="'https://placehold.jp/150x150.png?text=' + ar"></a></li>
        </ul>
      </nav>
    </div>
    <div class="wrap">
      <h3>おすすめラインナップ</h3>
      <nav>
        <ul>
          <li v-for="(ar, i) in arrImage2"><a :href="'/' + arrLink2[i] + '/'"><img :src="'https://placehold.jp/150x150.png?text=' + ar"></a></li>
        </ul>
      </nav>
    </div>
  </div>
</template>