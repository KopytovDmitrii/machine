<template>
<span>
  <span v-if="!!title">{{title}} </span>
  <a href="tel:+79259886307" :class="{ white: envers }">+7(925) 988-63-07 ☎</a>
</span>
  
</template>

<script>
export default {
  name: 'Number',
  props: {
    title: String,
    envers: Boolean
  },
}
</script>

<style scoped lang="scss">
  a{
    text-decoration: none;
    color: black
  }
  .white{
    color: white
  }
</style>
