<template>
  <div class="wrapper">
    <Main/>
    <Descriptions/>
    <CallMe/>
  </div>
</template>
W
<script>
import Main from './components/main/Main.vue';
import Descriptions from './components/descriptions/Descriptions.vue';
import CallMe from './components/CallMe.vue';

export default {
  name: 'Content',
  props: {},
  components: {
    Main,
    Descriptions,
    CallMe,
  },
}
</script>

<style scoped>
</style>
