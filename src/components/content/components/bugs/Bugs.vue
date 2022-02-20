<template>
  <div class="block-wrapper descriptions">
      <div class="content-wrapper descriptions-content">
          <div class="content">
            <div class="title">
              <span>Основные неисправности</span>
              <div class="border"></div>
            </div>
            <div class="list">
              <div class="listWrap">
                <BugItem
                  v-for="(bug, index) in bugs"
                  :key='index'
                  :title="bug.title"
                  :list="bug.list"
                  :src="bug.src"
                  :className="bug.className"
                  :isBorder="bug.isBorder"
                  :component="bug.component"
                />
              </div>
            </div>
          </div>
      </div>
  </div>
</template>

<script>
import BugItem from './components/BugItem.vue';

export default {
  name: 'Bugs',
  props: {},
  components: {
    BugItem,
  },
  data: () => ({
    bugs: [
      {
        title: 'Не сливает воду',
        list: [
          "Устранение засора",
          "Замена фильтра сливного насоса",
          "Замена помпы",
        ],
        src: './img/water.png',
        className: 'first',
        isBorder: true,
      },
      {
        title: 'Не отжимает',
        list: [
          "Замена электронного модуля",
          "Замена ремня привода барабана",
          "Замена датчика уровня воды",
          "Замена амортизаторов"
        ],
        src: './img/rem.png',
        className: 'second',
        isBorder: false,
      },
      {
        title: 'Протекает',
        list: [
          "Замена помпы",
          "Замена сливного шланга",
          "Замена манжеты",
          "Замена патрубков"
        ],
        src: './img/water.png',
        className: 'third',
        isBorder: false,
      },
      {
        title: 'Не греет воду',
        list: [
          "Замена ТЭНа",
          "Замена температурного датчика"
        ],
        src: './img/temp.png',
        className: 'fourth',
        isBorder: false,
      },
      {
        title: 'Не набирает воду',
        list: [
          "Устранение засора",
          "Замена заливного клапана",
          "Замена датчика уровня воды"
        ],
        src: './img/rem.png',
        className: 'fifts',
        isBorder: false,
      },
      {
        title: 'Шумит',
        list: [
          "Удаление постороннего предмета",
          "Замена амортизаторов",
          "Замена подшипников"
        ],
        src: './img/rem.png',
        className: 'sixth',
        isBorder: false,
      },
      {
        component: 'BannerMini',
        className: 'banner',
        isBorder: true,
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
    width: 100%;
    @media screen and (max-width: 900px) {
      padding-right: 00px;
      padding-left: 00px;
    }
    .title{
      font-size: 36px;
      padding: 4px;
      font-weight: bold;
      margin-bottom: 50px;
      @media screen and (max-width: 900px) {
        font-size: 26px;
        @media screen and (max-width: 900px) {
        padding-left: 20px;
      }
      }
      .border{
        width: 170px;
        margin-left: 63px;
        border-bottom: 5px solid rgba(0,0,170,1);
        margin-top: 8px;
      }
    }
    .list{
      padding-left: 65px;
      padding-right: 65px;
      @media screen and (max-width: 900px) {
        padding-left: 0px;
        padding-right: 0px;
      }
      .listWrap{
        display: flex;
        flex-wrap: wrap;
        -webkit-box-shadow: 0px 3px 13px 0px rgba(34, 60, 80, 0.2);
        -moz-box-shadow: 0px 3px 13px 0px rgba(34, 60, 80, 0.2);
        box-shadow: 0px 3px 13px 0px rgba(34, 60, 80, 0.2);
      }
      
    }
  }
}


</style>
