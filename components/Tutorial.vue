<!-- Please remove this file from your project -->
<template>
  <div>
    <test-component :header="title"></test-component>
    <button @click="changeTitle">Test</button>
  </div>
</template>

<script>
import TestComponent from './TestComponent.vue'
export default {
  components: { TestComponent },
  data() {
    return {
      name: "test",
      counter: this.$store.state.counter,
      title: "The Title"
    }
  },

  methods: {
    test() {
      console.log("created", this.counter)
      this.$store.commit('increment')
      console.log("counter", this.counter)
      console.log("state counter", this.$store.state.counter)
      this.counter = this.$store.state.counter
      
    },
    changeTitle() {
      this.title = "new one"
    }
  },

  created: function () {
    this.test()
  },
  watch: {
    counter: function() {
      console.log("changing")
      return this.counter
    }
  },

  computed: {
    counterTest() {
      return this.$store.state.counter
    }
  }
}
</script>
