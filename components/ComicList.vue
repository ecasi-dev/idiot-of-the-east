<template>
  <div class="comic-list-wrapper">
    <div class="comic-list">
      <div v-for="(comic, index) in comicList" :key="index" class="comic">
        <h2>{{ comic.title }}</h2>
        <img :src="comic.comicImageList[0]" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      comicList: [
        {
          title: 'Title 1',
          comicImageList: [
            'https://i.lensdump.com/i/tzKCsD.md.webp',
            'https://i1.lensdump.com/i/tzKgVT.webp',
            'https://i1.lensdump.com/i/tzKgVT.webp',
          ],
        },
        {
          title: 'Title 2',
          comicImageList: [
            'https://i1.lensdump.com/i/tzBH45.png',
            'https://i1.lensdump.com/i/tzBH45.png',
            'https://i1.lensdump.com/i/tzBH45.png',
          ],
        },
        {
          title: 'Title 3',
          comicImageList: [
            'https://i1.lensdump.com/i/tzBH45.png',
            'https://i1.lensdump.com/i/tzBH45.png',
            'https://i1.lensdump.com/i/tzBH45.png',
          ],
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.comic-list-wrapper {
  background: #cbecff;

  .comic-list {
    text-align: center;
    width: 95%;
    margin: auto;

    .comic {
      margin: 20px auto;

      h2 {
        background: grey;
      }

      img {
        width: 100%;
        display: block;
      }
    }
  }
}
</style>
