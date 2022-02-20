<template>
    <div class="callMe">
      <h3 class="title">Остались вопросы?</h3>
      <p>Звоните и Наш мастер проконсультирует Вас!</p>
      <btn
        text="Консультация"
        numberTitle="Звоните:"
        mini
        envers
      />
    </div>
</template>

<script>
import btn from '../../../../UI/btn.vue';
export default {
  name: 'BannerMini',
  components: {
    btn
  },
  props: {}
}
</script>

<style scoped lang="scss">
.callMe{
  height: 90%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding-bottom: 20px;
  color: white;
  p{
    font-size: 14px;
  }
  .title{
    font-size: 18px;
    padding-top: 0;
  }
}
</style>
