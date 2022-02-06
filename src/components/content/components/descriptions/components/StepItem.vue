<template>
  <div class="wrap">
    <div class="number">{{number}}</div>
    <div class="divaider"></div>
    <div class="content">
      <div class="title">{{title}}</div>
      <div class="subtitle">{{subtitle}}</div>
    </div>
  </div>
</template>
W
<script>
export default {
  name: 'StepItem',
  props: {
    number: String,
    title: String,
    subtitle: String,
  }
}
</script>

<style scoped lang="scss">
.wrap{
  display: flex;
  flex-direction: row;
  min-height: 60px;
  .number{
    width: 60px;
    padding: 4px;
    font-size: 35px;
    font-weight: bold;
    color: grey;
  }
  .divaider{
    width: 0px;
    border-left: 5px solid rgba(0,0,170,1);
  }
  .content{
    flex: 1;
    padding: 4px;
    display: flex;
    flex-direction: column;
    margin-left: 25px;
    .title{
      font-size: 22px;
      font-weight: 600;
      margin-bottom: 5px;
    }
    .subtitle {
      font-size: 18px;
      margin-bottom: 20px;
    }
  }

}
</style>
