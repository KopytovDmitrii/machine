<template>
   <div class="block-wrapper">
    <div class="content-wrapper callMe">
      <h2 class="title">Сломалась машинка? Звоните Нам!</h2>
      <div class="btn callMaster">
        <span>Вызвать мастера</span>
        <div class="arrow"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CallMe',
  props: {}
}
</script>

<style scoped lang="scss">
.callMe{
  border-top: 2px solid rgba(0,0,170,1);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 300px;
  margin-top: 35px;
  .title{
    padding: 30px;
    text-align: center;
  }
  .callMaster{
    position: relative;
    .arrow{
      position: absolute;
      top: -45px;
      left: -190px;
      width: 168px;
      height: 80px;
      background-image: url('./../../../assets/arrow.png');
      background-position: center center;
      background-repeat: no-repeat;
      background-size: cover;
    }
  }
}
</style>
