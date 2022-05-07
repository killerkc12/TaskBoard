<template>
  <div class="header">
    <div class="header__left">
      <img :src="logoUrl" alt="">
    </div>
    <div class="header__center">
     <!-- TODO: Add Search bar -->
    </div>
    <div class="header__right">
      header right
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderComponent',
  props: {

  },
  data() {
    return {
      logoUrl: 'https://tasksboard.com/img/logo.png'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 60px;
  background-color: #fff;
  box-shadow: 0px 2px 4px -1px rgba(0,0,0,0.2);
}

.header__left {
  box-sizing: border-box;
}

.header__left img {
  display: block;
  margin-left: 20px;
  height: 30px;
  width: 30px;
}

</style>
