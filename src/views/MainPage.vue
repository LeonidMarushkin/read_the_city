<template>
  <div class="main">
    <HeaderComponent />
    <div class="cardFrame">
      <BookCardVue v-for="(bookData, index) in bookCardData" v-bind:key="index" :author="bookData.author"
        :title="bookData.title" :imageSource="bookData.imageSource" />
    </div>
  </div>
</template>

<script>
import BookCardVue from '@/components/elements/BookCard.vue'
import HeaderComponent from '@/components/blocks/HeaderComponent.vue';
// import { ref } from 'vue'
export default {
  name: 'MainPage',
  components: {
    BookCardVue,
    HeaderComponent
  },
  data() {
    return {
      bookCardData: [
        {
          author: 'Франк Экстанази',
          title: 'Skyrim. Как продать игру 10 раз',
          imageSource: require('@/assets/img/image1.png')
        },
        {
          author: 'Сергей Анисимов',
          title: 'Поисковое продвижение сайтов',
          imageSource: require('@/assets/img/image2.png')
        },
        {
          author: 'Татьяна Магарина',
          title: 'Английский для дизайнеров',
          imageSource: require('@/assets/img/image3.png')
        },
        {
          author: 'Шон Адамс',
          title: 'Дизайн и цвет. Практикум',
          imageSource: require('@/assets/img/image4.png')
        },
      ]
    }
  },
  props: {
  },
  setup() {
  }
}
</script>

<style lang="scss" scoped>
.cardFrame {
  display: flex;
  align-items: flex-start;
  gap: 26px;
  justify-content: center;
}
</style>
