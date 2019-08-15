<template>
  <div contenteditable="true" class="flex-foo p-2" @input="updateInput" v-html="value"></div>
</template>

<script>
export default {
  props: {
    value: {
      type: String,
      default: ""
    }
  },
  model: {
    prop: "value",
    event: "input"
  },
  data() {
    return {
    }
  },
  methods: {
    updateInput() {
      console.log(this.$el.innerText);
      this.$emit('input', this.$el.innerText)
    }
  }
}

</script>

<style>

</style>
