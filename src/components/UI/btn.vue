<template>
  <div class="btnwrap">
    <div class="btn" @click="clickBtn">
      <span>{{text}}</span>
      <div v-if="isArrow" class="arrow"></div>
    </div>
    <Number class="btn-number" v-if="isNumber" :title="numberTitle" />
  </div>
</template>

<script>
import Number from './Number.vue';
export default {
  name: 'btn',
  components: {
    Number
  },
  data: ()=>({
    isNumber: false,
  }),
  props: {
    text: String,
    isArrow: Boolean,
    numberTitle: String
  },
  methods: {
    clickBtn() {
      this.isNumber = !this.isNumber
    }
  }
}
</script>

<style scoped lang="scss">
 .btn{
    width: 300px;
    height: 50px;
    background: rgba(0,0,170,1);
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    font-size: 15px;
    text-transform: uppercase;
    font-weight: bold;
    color: white;
    letter-spacing:2px;
    cursor: pointer;
    position: relative;
    -webkit-touch-callout: none; /* iOS Safari */
    -webkit-user-select: none; /* Safari */
     -khtml-user-select: none; /* Konqueror HTML */
       -moz-user-select: none; /* Old versions of Firefox */
        -ms-user-select: none; /* Internet Explorer/Edge */
            user-select: none; /* Non-prefixed version, currently
                                  supported by Chrome, Edge, Opera and Firefox */
    .arrow{
      position: absolute;
      top: -45px;
      left: -190px;
      width: 168px;
      height: 80px;
      background-image: url('../../assets/arrow.png');
      background-position: center center;
      background-repeat: no-repeat;
      background-size: cover;
    }
  }

  .btnwrap{
    position: relative;
    .btn-number{
      position: absolute;
      left: 42px;
      bottom: -23px;
    }
  }
</style>
