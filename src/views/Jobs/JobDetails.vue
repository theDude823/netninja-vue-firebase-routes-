<template>
  <h1 class="text-red-400">Job Details Page</h1>
  <div>The job id is {{ $route.params.id }}</div>
</template>

<script>
export default {
  data() {
    return {
      id: this.$route.params.id,
    };
  },
};
</script>

<style scoped></style>
