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
import Number from './UI/Number.vue';
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
    @media screen and (max-width: 900px) {
        height: 50px;
    }
    .header-content{
        display: flex;
        justify-content: space-between;
        @media screen and (max-width: 900px) {
            padding-left: 10px;
            padding-right: 10px;
        }

        .phone{
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 18px;
            font-weight: bold;

            @media screen and (max-width: 900px) {
                font-size: 16px!important;
            }
        }
    }
    .region{
        font-size: 18px;
        font-weight: normal;
        @media screen and (max-width: 900px) {
            font-size: 16px!important;
        }
    }
}
</style>
