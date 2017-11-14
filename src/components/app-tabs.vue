<template>
  <div class="tabs">
    <div class="tab-head-box">
      <div v-for="tab, i in tabs" v-on:click="active = i.toString()" v-bind:class="{ active: active == i }" class="tab-head">
        <div class="tab-head-title">{{ tab.head }}</div>
        <div class="tab-head-subtitle" v-if="tab.subtitle">{{ tab.subtitle }}</div>
      </div>
    </div>
    <div class="tab-body-box">
      <div v-for="tab, i in tabs" v-bind:class="{ active: active == i }" class="tab-body">
        <slot v-bind:name="tab.component">this is slot {{ i }}</slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app-tabs',
  props: ['tabs'],
  data: () => ({
    active: '0'
  })
}
</script>

<style lang="scss" scoped>
.tabs {
  .tab-head-box {
    display: flex;
    .tab-head {
      flex-grow: 1;
      text-align: center;
      padding: 20px 10px 6px;
      border-bottom: 1px solid #ddd;
      cursor: pointer;
      &.active {
        border-bottom: 1px solid #E62B1E;
      }
      .tab-head-title {
        font-weight: 500;
      }
      .tab-head-subtitle {
        color: #888;
        font-size: 13px;
        margin-top: 4px;
      }
    }
  }
  .tab-body {
    display: none;
    padding: 20px;
    line-height: 1.6;
    &.active {
      display: block;
    }
  }
  .svg-container {
    
  }
}
</style>
