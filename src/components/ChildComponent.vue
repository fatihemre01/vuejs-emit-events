<template>
  <h1>{{ title }}</h1>
  <input type="text" v-model="newTitle" />
  <button @click="changeTitle()">Change title</button>
</template>

<script>
export default {
  name: "ChildComponent",
  props: {
    title: String,
  },
  data() {
    return {
      newTitle: "",
    };
  },
  methods: {
    changeTitle() {
      this.$emit("titleChanging", this.newTitle);
    },
  },
};
</script>
