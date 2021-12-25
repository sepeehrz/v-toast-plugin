<template>
  <div class="hello">
    <button @click="show">open</button>
    <button @click="close">close</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    show() {
      this.$toast.success().showSimple('hello world');
    },
    close() {
      this.$toast.destroy();
    },
  },
};
</script>
<style scoped></style>
