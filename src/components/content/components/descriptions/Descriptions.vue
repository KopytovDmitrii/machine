<template>
  <div class="block-wrapper descriptions">
      <div class="content-wrapper descriptions-content">
          <div class="content">
            <div class="title">
              <span>Спектр услуг</span>
              <div class="border"></div>
            </div>
            <div class="list">
              <StepItem
                v-for="(step, index) in steps"
                :key='index'
                :number="step.number"
                :title="step.title"
                :subtitle="step.subtitle"
              />
            </div>
          </div>
          <div class="infograph">
            <div class="border">
              <div class="img"></div>
            </div>
          </div>
      </div>
  </div>
</template>

<script>
import StepItem from './components/StepItem.vue';

export default {
  name: 'Descriptions',
  props: {},
  components: {
    StepItem,
  },
  data: () => ({
    steps: [
      {
        number: '01',
        title: 'Выезд на дом',
        subtitle: 'Обсудим удобное для Вас время',
      },
      {
        number: '02',
        title: 'Диагностика',
        subtitle: 'Установим причину неисправности и определим износ составляющих',
      },
      {
        number: '03',
        title: 'Профилактика',
        subtitle: 'Прочистим и устраним засоры',
      },
      {
        number: '04',
        title: 'Замена комплектующих',
        subtitle: 'Найдем любые запчасти для Вашей машинки',
      },
    ]
  })
}
</script>

<style scoped lang="scss">
.descriptions {
  padding-top: 50px;
  padding-bottom: 50px;
  @media screen and (max-width: 900px) {
    padding-top: 20px;
    padding-bottom: 20px;
  }
}
.descriptions-content{
  display: flex;
  flex-direction: row;

  .content{
    flex: 1;
    padding-right: 10px;
    @media screen and (max-width: 900px) {
      padding-right: 20px;
      padding-left: 20px;
    }
    .title{
      font-size: 42px;
      padding: 4px;
      font-weight: bold;
      margin-bottom: 50px;
      @media screen and (max-width: 900px) {
        font-size: 30px;
      }
      .border{
        width: 170px;
        margin-left: 63px;
        border-bottom: 5px solid rgba(0,0,170,1);
        margin-top: 8px;
      }
    }
  }
  .infograph{
    flex: 1;
    padding-left: 70px;
     @media screen and (max-width: 900px) {
      display: none;
    }
    .border{
      border: 5px solid rgba(0,0,170,1);
      width: 412px;
      height: 535px;
      position: relative;
      .img{
        position: absolute;
        bottom: 0px;
        left: -80px;
        width: 510px;
        height: 455px;
        background-image: url('./../../../../assets/machine.png');
        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;
      }
    }
  }

}


</style>
