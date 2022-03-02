<template>
  <div>
    <a
      class="name-admin"
      @click="jumpDetail(admin.id)"
      v-for="admin in listAdmin"
      :key="admin.id"
      >{{ admin.name }}</a
    >
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
    console.log(this.param);
  },
  methods: {
    jumpDetail(parameter) {
      this.$router.push(`/about/${parameter}`);
    },
  },
};
</script>
<style>
.name-admin {
  color: coral;
  display: flex;
  cursor: pointer;
  justify-content: center;
  font-size: 20px;
  margin: 5px;
}
</style>
