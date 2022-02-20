<template>
   <div class="block-wrapper">
    <div class="content-wrapper moreBugs">
      <h2 class="title">Частые неисправности стиралок</h2>
      <div class="content">
        
        <p>Ремонт стиральных машин проводится по разным причинам. Чаще всего в технике ломаются:</p>
        <ul>
          <li
            v-for="(item, index) of list"
            :key="index"
          >{{item}}</li>
        </ul>
        <p>Наш специалист оперативно устранят любые поломки. Чтобы вызвать мастера, звоните. Специалист выезжает сразу после заказа либо в любое удобное для вас время.</p>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: 'MoreBugs',
  data: () => ({
    list: [
      "Сливная помпа. Ресурс насосов не более 5 лет активной эксплуатации.",
      "Термодатчик. Они часто ломаются уже после 2-х лет работы.",
      "ТЭН. Нагревательный элемент перегорает от жесткой воды, т. е. из-за накипи.",
      "Электронный модуль. Выходит из строя, в основном, из-за скачков напряжения."
    ]
  }),
  props: {}
}
</script>

<style scoped lang="scss">
.moreBugs{
  display: flex;
  flex-direction: column;
  justify-content: center;
  
  padding-top: 50px;
  padding-bottom: 50px;
  @media screen and (max-width: 900px) {
    padding-top: 20px;
    padding-bottom: 20px;
  }
  .title{
      padding-top: 0;
      color: #db073d;
      font-size: 28px;
      @media screen and (max-width: 900px) {
        font-size: 26px;
        padding-left: 15px;
      }
    }
  .content{
    margin-top: 15px;
    padding-left: 65px;
    padding-right: 65px;
    @media screen and (max-width: 900px) {
      padding-left: 40px;
      padding-right: 40px;
    }
    p{
      font-size: 18px;
      margin-top: 15px;
    }
    ul{
      margin-top: 15px;
      list-style: none;
      li{
        margin-left: 15px;
        margin-top: 7px;
        &::before{
          content: ' ';
          position: absolute;
          width: 4px;
          height: 4px;
          border-radius: 50%;
          margin: 9px 0 0 -15px;
          overflow: hidden;
          background: #db073d;
        }
      }
    }
    
  }
  
}
</style>
