<template>
  <div class="wrap">
    <h1 class="title">Ремонт стиральных машин</h1>
    <h2 class="subtitle">Сертифицированный мастер восстановит работу Вашей стиральной машины</h2>
    <div class="btn">заказать ремонт</div>
  </div>
</template>
W
<script>
export default {
  name: 'Banner',
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

  .title{
    font-size: 30px;
    font-weight: bold;
    text-align: center;
  }
  .subtitle{
    font-size: 22px;
    text-align: center;
  }
 
}
</style>
