<template>
  <div class="home-bottom">
    <div class="container">
      <h3>About TED</h3>
      <p>
      TED is a nonpartisan nonprofit devoted to spreading ideas, usually in the form of short, powerful talks. TED began in 1984 as a conference where Technology, Entertainment and Design converged, and today covers almost all topics — from science to business to global issues — in more than 110 languages. Meanwhile, independently run TEDx events help share ideas in communities around the world.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app-home-bottom'
}
</script>

<style lang="scss" scoped>
.home-bottom {
  display: flex;
  justify-content: center;
  border-top: 2px solid #ddd;
  padding: 60px 10px;
  margin-top: 60px;
  background: white;
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    &>* {
      max-width: 500px;
    }
    h3 {
      color: #676767;
      font-size: 34px;
      font-weight: 300;
      margin-bottom: 30px;
    }
    p {
      text-align: center;
      color: #898989;
      line-height: 1.8;
      font-size: 14px;
    }
  }
}
</style>
