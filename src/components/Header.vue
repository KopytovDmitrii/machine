<template>
  <div class="block-wrapper header">
      <div class="content-wrapper header-content">
          <h1 class="region">Регион: Москва</h1>
          <div class="phone"><Number/></div>
      </div>
  </div>
</template>
W
<script>
import Number from './Number.vue';
export default {
  name: 'Header',
  components: {
      Number
  },
  props: {}
}
</script>

<style scoped lang="scss">
.header{
    background: white;
    width: 100%;
    height: 90px;
    .header-content{
        display: flex;
        justify-content: space-between;

        .phone{
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 18px;
            font-weight: bold;
        }
    }
    .region{
        font-size: 20px;
        font-weight: normal;
    }
}
</style>
