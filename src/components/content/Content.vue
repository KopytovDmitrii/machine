<template>
  <div class="wrapper">
    <Main/>
    <Descriptions/>
    <Bugs/>
    <MoreBugs/>
    <CallMe/>
  </div>
</template>
W
<script>
import Main from './components/main/Main.vue';
import Descriptions from './components/descriptions/Descriptions.vue';
import CallMe from './components/CallMe.vue';
import Bugs from './components/bugs/Bugs.vue'
import MoreBugs from './components/MoreBugs.vue'

export default {
  name: 'Content',
  props: {},
  components: {
    Main,
    Descriptions,
    CallMe,
    Bugs,
    MoreBugs,
  },
}
</script>

<style scoped>
.wrapper{
  overflow: hidden;
}
</style>
