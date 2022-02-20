<template>
  <div class="btnwrap">
    <div class="btn" :class='{miniBth: mini}' @click="clickBtn" v-if="!isMobile">
      <span>{{text}}</span>
      <div v-if="isArrow" class="arrow"></div>
    </div>
    <a v-else class="btn" href="tel:+79259886307">
        <span>{{text}}</span>
        <div v-if="isArrow" class="arrow"></div>
    </a>
    <Number class="btn-number" envers :class='{miniNumber: mini}' v-if="isNumber" :title="numberTitle" />
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
    isMobile: false,
  }),
  props: {
    text: String,
    isArrow: Boolean,
    numberTitle: String,
    mini: Boolean,
    envers: Boolean
  },
  methods: {
    clickBtn() {
      this.isNumber = !this.isNumber
    },
    setIsMobile() {
      console.log('123');
      let width = window.innerWidth;
      if (width <= 900) {
        this.isMobile = true;
      } else {
        this.isMobile = false;
      }
    }
  },
  mounted() {
    window.addEventListener('resize', this.setIsMobile);
    this.setIsMobile();
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
    text-decoration: none;
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

  .miniBth{
    max-width: 200px;
    min-width: 150px;
    width: auto;
    height: 40px;
    font-size: 11px;
  }

  .btnwrap{
    position: relative;
    .btn-number{
      position: absolute;
      left: 42px;
      bottom: -23px;
    }
    .miniNumber{
      left: 12px;
      bottom: -20px;
      font-size: 13px;
    }
  }
</style>
