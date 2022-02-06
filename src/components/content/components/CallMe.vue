<template>
   <div class="block-wrapper">
    <div class="content-wrapper callMe">
      <h2 class="title">Сломалась машинка? Звоните Нам!</h2>
      <btn
        text="Вызвать мастера"
        :isArrow="true"
        numberTitle="Звоните:"
      />
    </div>
  </div>
</template>

<script>
import btn from '../../UI/btn.vue';
export default {
  name: 'CallMe',
  components: {
    btn
  },
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
    padding-top: 0;
    text-align: center;
  }
}
</style>
