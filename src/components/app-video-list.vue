<template>
  <div class="video-list">
    <ol>
      <li v-for="item in list">
        <div class="video">
          <div class="video-image" v-bind:style="{ backgroundImage: `url(${item.backgroundUrl})` }"></div>
          <div class="video-length">{{ item.length }}</div>
        </div>
        <div class="item-meta">
          <div class="item-title">{{ item.title }}</div>
          <div class="item-views">{{ item.views }} views</div>
        </div>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: 'app-video-list',
  data: () => ({
    list: [
      {
        title: `We need to talk about an injustice`,
        views: '3.9M',
        length: '23:41',
        backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/537e4f8ab618be6cf3d40287aa04df004f543c2f_1600x1200.jpg?op=%5E&amp;c=288%2C162&amp;gravity=t&amp;u%5Br%5D=2&amp;u%5Bs%5D=0.5&amp;u%5Ba%5D=0.8&amp;u%5Bt%5D=0.03&amp;quality=82&amp;w=288&amp;h=162'
      },
      {
        title: `How jails extort the poor`,
        views: '962k',
        length: '12:43',
        backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/4658539c6f725bfe3d2681f733f16237ac2f1527_2880x1620.jpg?op=%5E&amp;c=288%2C162&amp;gravity=t&amp;u%5Br%5D=2&amp;u%5Bs%5D=0.5&amp;u%5Ba%5D=0.8&amp;u%5Bt%5D=0.03&amp;quality=82&amp;w=288&amp;h=162'
      },
      {
        title: `How we're priming some kids for college — and others for prison`,
        views: '1.6M',
        length: '16:04',
        backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/15eec689c9a2eed8c471eb5ce5dda72de49a6cac_2880x1620.jpg?op=%5E&amp;c=288%2C162&amp;gravity=t&amp;u%5Br%5D=2&amp;u%5Bs%5D=0.5&amp;u%5Ba%5D=0.8&amp;u%5Bt%5D=0.03&amp;quality=82&amp;w=288&amp;h=162'
      }
    ]
  })
}
</script>

<style lang="scss" scoped>
li {
  display: flex;
  .video {
    flex: 0 0 40%;
    position: relative;
    .video-image {
      padding-bottom: 56.25%;
      background-size: cover;
      margin-right: 8px;
    }
    .video-length {
      position: absolute;
      right: 8px;
      bottom: 2px;
      background: black;
      border-radius: 2px;
      color: white;
      padding: 2px 6px;
      font-size: 12px;
    }
  }
  .item-meta {
    flex: 0 0 60%;
    .item-title {
      line-height: 1.1;
      font-weight: 600;
      margin-bottom: 8px;
    }
    .item-views {
      font-size: 13px;
      color: #777;
    }
  }
  &+li {
    margin-top: 16px;
  }
}
</style>
