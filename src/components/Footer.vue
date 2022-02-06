<template>
  <div class="block-wrapper footer">
    <div class="content-wrapper footer-content">
      <div class="content">
        <div class="region">Регион оказания услуг: Москва</div>
        <div class="phone">Контактный телефон: <Number/></div>
      </div>
      <div class="devider">
          <div> © 2021–2022 </div> 
          <div>Вся представленная на сайте информация носит информационный характер и не является публичной офертой</div>
      </div>
    </div>
  </div>
</template>
<script>
import Number from './Number.vue';
export default {
  name: 'Footer',
  components: {
    Number
  },
  props: {}
}
</script>

<style scoped lang="scss">
.footer{
  background: #abcadc;
  height: 150px;
  .footer-content{
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    .devider{
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      font-size: 14px;
      border-top: 1px solid grey;
      padding-bottom: 10px;
      padding-top: 5px;
    }
    .content{
      padding-top: 20px;
      .phone{
        margin-top:5px
      }
    }
  }
  
}

</style>
