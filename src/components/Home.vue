<template>
  <div class="container">
    <div class="home-header" style="background-image: linear-gradient(159deg, rgba(0 ,0 ,0, .9), rgba(0, 0, 0, .2) 20rem), url(https://pi.tedcdn.com/r/s3.amazonaws.com/talkstar-photos/uploads/87977bdd-8faf-4a5a-9ac4-118d31e7e532/TeresaNjoroge_2017W-embed.jpg?blur=0%2C10&amp;cb=20160613&amp;quality=63&amp;u=&amp;w=150);">
      <div v-for="item, index of list" class="item" v-on:click="rotate(index)">
        <div class="item-image" v-bind:style="{ backgroundImage: `url(${item.backgrondUrl})` }"></div>
        <div class="item-meta">
          <div class="item-title">{{ item.title }}</div>
          <div class="item-speaker">{{ item.speaker }} / <span>{{ item.position }}</span></div>
          <div class="item-description">{{ item.description }}</div>
        </div>
      </div>
      <div class="item">
      </div>
    </div>
    <app-strips></app-strips>
    <app-home-bottom></app-home-bottom>
  </div>
</template>

<script>
import AppStrips from './app-strips'
import AppHomeBottom from './app-home-bottom'

export default {
  name: 'home',
  components: { AppStrips, AppHomeBottom },
  data: function () {
    return {
      list: [
        {
          backgrondUrl: 'https://pi.tedcdn.com/r/s3.amazonaws.com/talkstar-photos/uploads/87977bdd-8faf-4a5a-9ac4-118d31e7e532/TeresaNjoroge_2017W-embed.jpg?cb=20160613&amp;quality=60&amp;u=&amp;w=1400',
          title: `What I learned serving time for a crime I didn't commit`,
          speaker: 'Teresa Njoroge',
          position: 'Criminal and social justice reform advocate',
          description: 'TED Talk: Daniel Kish explains how he uses sound to navigate the world'
        },
        {
          backgrondUrl: 'https://pi.tedcdn.com/r/tedcdnpe-a.akamaihd.net/images/ted/9d9e218a26b00bd5a0eb2f69f9a44e768fdebc26_2880x1620.jpg?cb=20160511&amp;h=500&amp;quality=90&amp;w=',
          title: `How to see with sound`,
          speaker: 'Daniel Kish',
          position: 'Perceptual navigation specialist',
          description: 'TED Talk: Daniel Kish explains how he uses sound to navigate the world'
        },
        {
          backgrondUrl: 'https://pi.tedcdn.com/r/tedcdnpf-a.akamaihd.net/images/playlists/find_your_purpose_1200x627.jpg?cb=20160511&amp;h=500&amp;quality=90&amp;w=',
          title: `7 talks to help you find your purpose`,
          speaker: 'Playlist',
          position: '7 talks',
          description: 'Not sure what to do with your one precious life? These talks can help you discover your path'
        },
        {
          backgrondUrl: 'https://pi.tedcdn.com/r/s3.amazonaws.com/talkstar-photos/uploads/757d61e4-4717-4e0f-acb0-5ccad04d6a57/JacksonBird_2017S-embed.jpg?cb=20160613&quality=60&u=&w=1400',
          title: `How to talk (and listen) to transgender people`,
          speaker: 'Jackson Bird',
          position: 'Digital storyteller, activist',
          description: 'Gender should be the least remarkable thing about someone, but transgender people are still too often misunderstood.'
        }
      ]
    }
  },
  methods: {
    rotate: function (index) {
      if (index === 0) {
        this.$router.push('video')
      }
      if (index === 1) {
        var firstItem = this.list.shift()
        this.list.push(firstItem)
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  background-color: #fafafa;
}
.home-header {
  height: 400px;
  background-size: cover;
  display: flex;
  justify-content: space-around;
  align-items: flex-end;
  .item {
    position: relative;
    .item-image {
      background-size: cover;
    }
    .item-meta {
      position: absolute;
      width: 90%;
      margin-left: -14%;
      background: rgba(0, 0, 0, .8);
      padding: 10px;
      display: none;
    }
    .item-title {
      color: white;
      font-size: 36px;
      line-height: 34px;
      margin-bottom: 12px;
    }
    .item-speaker {
      color: white;
      font-size: 16px;
      span {
        font-size: 14px;
        color: #ccc;
      }
    }
    .item-description {
      margin-top: 12px;
      color: #999;
    }
  }
  .item:nth-child(1) {
    flex: 0 0 56%;
    cursor: pointer;
    .item-image {
      height: 346px;
    }
    .item-meta {
      top: 20%;
      left: 100%;
      display: block;
    }
  }
  .item:nth-child(2) {
    flex: 0 0 16%;
    opacity: .5;
    margin-bottom: 12px;
    .item-image {
      height: 100px;
    }
    &:hover {
      cursor: pointer;
      opacity: .9 !important;
    }
  }
  .item:nth-child(3) {
    flex: 0 0 10%;
    opacity: .2;
    margin-bottom: 18px;
    .item-image {
      height: 60px;
    }
  }
  .item:nth-child(4) {
    flex: 0 0 4%;
    opacity: 0;
    .item-image {
      height: 90px;
    }
  }
}
</style>
