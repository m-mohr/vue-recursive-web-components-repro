<template>
  <span>
    {{ msg }}
    <HelloWorld v-if="!nested" msg="World" :nested="true" />
    <br />
    <QuitWorld v-if="!nested" />
  </span>
</template>

<script>
import QuitWorld from './QuitWorld.vue'

export default {
  name: 'HelloWorld',
  components: {
    QuitWorld
  },
  props: {
    msg: {
      type: String,
      default: "Hello"
    },
    nested: {
      type: Boolean,
      default: false
    }
  },
  mounted() {
    console.log(this.msg);
  }
}
</script>