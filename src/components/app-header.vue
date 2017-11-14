<template>
  <nav v-bind:class="{white: sticky, home: $route.path === '/'}">
    <div class="logo">
      <button class="guide" v-on:click="isOpen = !isOpen" v-on:blur="isOpen = false"><i class="fa fa-bars" aria-hidden="true"></i></button>
      <router-link to="/"><img src="../assets/logo.svg"></router-link>
      <router-link to="/"><span>Ideas worth spreading</span></router-link>
    </div>
    <div class="actions">
      <a href="#">Discover</a>
      <a href="#">Attend</a>
      <a href="#">Participate</a>
      <form>
        <input type="search" placeholder="Search">
        <button><i class="fa fa-search" aria-hidden="true"></i></button>
      </form>
      <button class="login">Sign In</button>
    </div>
    <aside v-bind:class="{open: isOpen}">
      <div class="side-column">
        <div class="nav-title">Watch</div>
        <a>
          <div>TED Talks</div>
          <p>Browse the library of TED talks and speakers</p>
        </a>
        <a>
          <div>Playlists</div>
          <p>100+ collections of TED Talks, for curious minds</p>
        </a>
        <a>
          <div>TED-Ed videos</div>
          <p>Watch, share and create lessons with TED-Ed</p>
        </a>
        <a>
          <div>TEDx Talks</div>
          <p>Talks from independently organized local events</p>
        </a>
        <a>
          <div>Surprise Me</div>
          <p>The easy option. Let us choose for you!</p>
        </a>
      </div>
      <div class="side-column">
        <div class="nav-title">About</div>
        <a>
          <div>Our organization</div>
          <p>Our mission, history, team, and more</p>
        </a>
        <a>
          <div>Conferences</div>
          <p>TED Conferences, past, present, and future</p>
        </a>
        <a>
          <div>Programs & initiatives</div>
          <p>Details about TED's world-changing initiatives</p>
        </a>
        <a>
          <div>Partner with TED</div>
          <p>Learn how you can partner with us</p>
        </a>
        <a>
          <div>TED Blog</div>
          <p>Updates from TED and highlights from our global community</p>
        </a>
      </div>
    </aside>
  </nav>
</template>

<script>
export default {
  name: 'app-header',
  data: () => ({
    isOpen: false,
    sticky: false
  }),
  methods: {
    handleScroll (e) {
      this.sticky = e.target.scrollingElement.scrollTop > 321
    }
  },
  created: function () {
    window.addEventListener('scroll', this.handleScroll)
  },
  destroyed: function () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="scss" scoped>
nav {
  height: 54px;
  background-color: #000;
  display: flex;
  justify-content: space-between;
  position: fixed;
  width: 100%;
  z-index: 4000;
  color: white;
  &.home { background-color: rgba(0, 0, 0, .2) }
  &.white {
    background-color: white;
    color: black;
    box-shadow: 0 0 8px rgba(0, 0, 0, .4);
    button { color: black; }
  }
}
.logo {
  display: flex;
  align-items: center;
  font-size: 18px;
}
.actions {
  display: flex;
  align-items: center;
  a {
    text-transform: uppercase;
    font-size: 14px;
    margin: 0 16px 0 0;
    padding: 10px;
    &:hover {
      text-shadow: 0 0 4px rgba(255, 255, 255, .5);
      background-color: rgba(0, 0, 0, .3);
    }
  }
}
button {
  background: none;
  border: none;
  border-radius: 0;
  cursor: pointer;
  color: white;
  &.guide, &.login {
    height: 54px;
  }
  &.guide {
    width: 54px;
    border-right: 1px solid black;
    font-size: 18px;
  }
  &.login {
    padding: 0 24px;
  }
  &:focus {
    outline: 0;
  }
}
aside {
  display: none;
  position: absolute;
  top: 55px;
  left: 0;
  padding: 10px;
  box-shadow: 0 0 8px rgba(0, 0, 0, .4);
  background: white;
  max-height: calc(100vh - 54px);
  overflow: scroll;
  .side-column {
    .nav-title {
      font-weight: 600;
      padding: 6px 10px;
      margin-bottom: 12px;
      border-bottom: 1px solid #eee;
      color: #555;
    }
    a {
      display: block;
      width: 240px;
      font-size: 14px;
      cursor: pointer;
      padding: 8px 10px;
      div {
        font-weight: 600;
        color: #000;
      }
      &:hover {
        background: #f4f4f4;
      }
      p { color: #888; }
    }
  }
  &.open {
    display: flex;
  }
}
</style>
