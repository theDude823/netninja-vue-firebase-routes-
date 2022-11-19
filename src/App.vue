<script>
import { RouterLink, RouterView } from "vue-router";
export default {
  methods: {
    redirect() {
      this.$router.push({ name: "home" });
    },
    back() {
      this.$router.go(-1);
    },
    forward() {
      this.$router.go(1);
    },
  },
};
</script>

<template>
  <header>
    <div class="flex flex-col bg-slate-500">
      <nav class="flex justify-around text-3xl">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink :to="{ name: 'about' }">About</RouterLink>
        <RouterLink :to="{ name: 'jobs' }">Jobs</RouterLink>
      </nav>
      <div class="flex justify-between">
        <button @click="redirect">Redirect</button>
        <button @click="back">Go Back</button>
        <button @click="forward">Go Forward</button>
      </div>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
.router-link-exact-active {
  @apply text-9xl;
}
</style>
