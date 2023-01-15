<template>
  <ChildComponent :title="title" @titleChanging="fatih($event)" />
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";
export default {
  name: "App",
  components: {
    ChildComponent,
  },
  data() {
    return {
      title: "Hello",
    };
  },
  methods: {
    fatih(newTitle) {
      this.title = newTitle;
    },
  },
};
</script>
