<template>
  <div class="comic-list-wrapper">
    <div class="comic-list">
      <div v-for="(comic, index) in comicList.values" :key="index" class="comic">
        <h2>{{ comic.title }}</h2>
        <img :src="comic[1]" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      comicList: [],
    }
  },

  async fetch() {
      this.comicList = await fetch(
        'https://sheets.googleapis.com/v4/spreadsheets/1MfsnN7IPw-iBIEy8fn4fEn6D6aQIiOQ8TQDCClcObsE/values/Sheet1?key=AIzaSyBeJ3Tr13K7dzwYs8tDIKcOMt-EWA8mSo8'
      ).then(res => res.json())
    },

  created(){
    
  }
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
