<template>
  <div>
    <h2 v-if="this.param.params.id === '1'">{{ listAdmin[0].name }}</h2>
    <h2 v-show="this.param.params.id === '2'">{{ listAdmin[1].name }}</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      param: this.$route,
      listAdmin: [
        { name: "Nolan", id: 1 },
        { name: "Nora", id: 2 },
      ],
    };
  },
  mounted() {
    console.log(this.param.params.id);
    console.log(this.param);
  },
};
</script>