// list of jobs
<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h2>{{ job.title }}</h2>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { title: "Ninja Ux designer", id: 1, details: "lorem" },
        { title: "Ninja Web dev", id: 2, details: "lorem" },
        { title: "Ninja Vue dev", id: 3, details: "lorem" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
//
