<template>
  <div class="container">
    <main>
      <div class="main-video"></div>
      <app-tabs v-bind:tabs="mainTab">
        <app-video-detail slot="video-detail"></app-video-detail>
        <app-video-transcript slot="video-transcript"></app-video-transcript>
        <app-video-reading-list slot="video-reading-list"></app-video-reading-list>
        <app-video-footnotes slot="video-footnotes"></app-video-footnotes>
        <app-video-comments slot="video-comments"></app-video-comments>
      </app-tabs>
    </main>
    <aside>
      <app-tabs v-bind:tabs="sideTab">
        <app-video-list slot="video-list"></app-video-list>
        <app-no-list slot="no-list"></app-no-list>
      </app-tabs>
    </aside>
  </div>
</template>

<script>
import AppTabs from './app-tabs'
import AppVideoList from './app-video-list'
import AppNoList from './app-no-list'
import AppVideoDetail from './app-video-detail'
import AppVideoTranscript from './app-video-transcript'
import AppVideoReadingList from './app-video-reading-list'
import AppVideoFootnotes from './app-video-footnotes'
import AppVideoComments from './app-video-comments'

export default {
  name: 'video',
  components: { AppTabs, AppVideoList, AppNoList, AppVideoDetail, AppVideoTranscript, AppVideoReadingList, AppVideoFootnotes, AppVideoComments },
  data: () => ({
    mainTab: [
      {
        head: 'Details',
        subtitle: 'About the talk',
        component: 'video-detail'
      },
      {
        head: 'Transcript',
        subtitle: '1 language',
        component: 'video-transcript'
      },
      {
        head: 'Reading list',
        subtitle: 'Further learning',
        component: 'video-reading-list'
      },
      {
        head: 'Footnotes',
        subtitle: 'Notes + references',
        component: 'video-footnotes'
      },
      {
        head: 'Comments',
        subtitle: 'Join the conversation',
        component: 'video-comments'
      }
    ],
    sideTab: [
      {
        head: 'Watch next',
        component: 'video-list'
      },
      {
        head: 'Your list(0)',
        component: 'no-list'
      }
    ]
  })
}
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  padding-top: 54px;
  main {
    flex: 0 0 66.66666666%;
    .main-video {
      width: 100%;
      padding-bottom: 56.25%;
      background-image: url('../assets/video.png');
      background-size: cover;
    }
  }
  aside {
    flex: 0 0 33.33333333%;
    background: #F2F2F2;
  }
}
</style>
