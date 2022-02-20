<template>
  <div class="wrap background" :class="[{ border: isBorder }, className]">
    <div class="cont-wrapper" v-if="!component">
      <div class="content">
        <div class="title">{{title}}</div>
        <ul class="list">
          <li
            v-for="(item, index) of list"
            :key="index"
          >{{item}}</li>
        </ul>
      </div>
      <img class="icon" :src="src">
    </div>
    <component :is="component"></component>
    
  </div>
</template>
<script>
import BannerMini from './BannerMini.vue';
export default {
  name: 'BugItem',
  components: {
    BannerMini
  },
  props: {
    title: String,
    list: Array,
    src: String,
    isBorder: Boolean,
    className: String,
    component: String,
  }
}
</script>

<style scoped lang="scss">
.border{
  border: 5px solid rgba(0,0,170,1)!important;
}
.background{
  background-position: right bottom;
  background-repeat: no-repeat;
  background-size: contain;
}
.first {
  background-image: url('../../../../../assets/bugfirst.png');
  width: 50%;
  @media screen and (max-width: 1050px) {
    background-image: none;
      width: 50%;
    &::after{
      content: '01';
    }
  }
  @media screen and (max-width: 900px) {
    background-image: none;
    width: 50%;
    &::after{
      content: '01';
    }
  }
}
.second {
  width: 25%;
  @media screen and (max-width: 900px) {
    width: 50%;
  }
  &::after{
    content: '02';
  }
}
.third {
  @media screen and (max-width: 900px) {
    width: 50%;
  }
  &::after{
    content: '03';
  }
  width: 25%;
}
.fourth {
  @media screen and (max-width: 900px) {
    width: 50%;
  }
  width: 25%;
  &::after{
    content: '04';
  }
}
.fifts {
  @media screen and (max-width: 900px) {
    width: 50%;
  }
  width: 25%;
  &::after{
    content: '05';
  }
}
.sixth {
  @media screen and (max-width: 900px) {
    width: 50%;
  }
  width: 25%;
  &::after{
    content: '06';
  }
}
.banner {
  @media screen and (max-width: 900px) {
    width: 100%;
    background-size: contain;
    background-position: right;
    background-color: #547989;
    height: 200px!important;
  }
  width: 25%;
  background-image: url('../../../../../assets/master.jpg');
  background-size: cover;
  background-position: right;
}
.wrap{
  
  min-height: 60px;
  padding: 20px;
  height: 280px;
  box-sizing: border-box;
  border: 1px solid rgba(171, 171, 171, 0.5);
  position: relative;
  &::after{
    position: absolute;
    bottom: 0;
    right: 5px;
    font-size: 80px;
    line-height: 90px;
    font-weight: bold;
    color: rgba(0,0,0,0.04);
    font-family: sans-serif;
  }
  .cont-wrapper{
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .icon{
    width: 40px;
    height: 40px;
  }
  
  .content{
    display: flex;
    flex-direction: column;
    .title{
      font-size: 18px;
      font-weight: 600;
      margin-bottom: 5px;
    }
    .list{
      margin-top: 10px;
      padding-left: 20px;
      li{
        margin-top: 8px;
        color: #71808a;
        font-size: 13px;
        font-weight: bold;
      }
    }
  }

}
</style>
