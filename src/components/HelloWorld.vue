<template>
  <div class="hello">
    <AR/>
  </div>
</template>

<script>
import AR from './AR';
export default {
  name: 'HelloWorld',
  components: {
    AR,
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
