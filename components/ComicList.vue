<template>
  <div class="comic-list-wrapper">
    <div class="comic-list">
      <div
        v-for="(comic, index) in comicList.values"
        :key="index"
        class="comic"
      >
        <h2>{{ comic[0] }}</h2>
        <p class="date">{{ comic[2] }}</p>
        <img :src="comic[1]" alt="" />
        <div class="sharebar">
          <div class="views">
            <img src="https://i3.lensdump.com/i/tzM99o.png" alt="views" />{{
              comic[3]
            }}
          </div>
          <button>Share</button>
        </div>
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
    ).then((res) => res.json())
  },

  created() {},
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@600;800&family=Mulish:wght@600&family=Roboto:wght@300;400;500;700&display=swap');

.comic-list-wrapper {
  font-family: 'Roboto', sans-serif;

  .comic-list {
    width: 90%;
    margin: auto;

    .comic {
      margin: 20px auto 0;
      padding-bottom: 30px;
      border-bottom: 1px solid rgb(208, 208, 208);

      h2 {
        font-weight: 400;
      }

      img {
        width: 100%;
        display: block;
      }

      .date {
        font-size: 14px;
        margin-bottom: 10px;
      }

      .sharebar {
        margin-top: 15px;
        display: flex;
        justify-content: space-between;

        .views{
            margin-left: 10px;
            display: flex;

            img{
                height: 20px;
                margin-right: 10px;
            }
        }

        button {
          border: none;
          background: none;
        }
      }
    }
  }
}
</style>
