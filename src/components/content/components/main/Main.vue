<template>
  <div class="block-wrapper mainImg">
    <div class="content-wrapper main-content">
      <Banner/>
    </div>
  </div>
</template>
W
<script>
import Banner from './components/Banner.vue';
export default {
  name: 'Main',
  components: {
    Banner
  },
  props: {}
}
</script>

<style scoped>
  .mainImg{
    height: 650px;
    background-image: url('./../../../../assets/main.jpg');
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  .main-content{
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
  }
</style>
