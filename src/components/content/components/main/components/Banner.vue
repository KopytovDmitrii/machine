<template>
  <div class="wrap">
    <h1 class="title">Ремонт стиральных машин</h1>
    <h2 class="subtitle">Сертифицированный мастер восстановит работу Вашей стиральной машины</h2>
    <btn
      text="заказать ремонт"
      numberTitle="Звоните:"
    />
  </div>
</template>
<script>
import btn from '../../../../UI/btn.vue';
export default {
  name: 'Banner',
  components: {
    btn
  },
  props: {}
}
</script>

<style scoped lang="scss">
.wrap{
  background: white;
  width: 500px;
  height: 350px;
  opacity: 0.8;
  padding: 40px;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  @media screen and (max-width: 900px) {
    max-width: 500px;
    height: 300px;
    width: auto;
  }

  .title{
    font-size: 30px;
    font-weight: bold;
    text-align: center;
     @media screen and (max-width: 900px) {
      font-size: 25px;
    }
  }
  .subtitle{
    font-size: 22px;
    text-align: center;
     @media screen and (max-width: 900px) {
      font-size: 18px;
    }
  }
 
}
</style>
