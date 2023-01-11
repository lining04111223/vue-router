<template>
  <div>
    <h1>Jobs</h1>
    <div v-for="job in jobs" :key="job.id">
      {{ job.title }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { title: "UX designer", id: 1 },
        { title: "web developer", id: 2 },
        { title: "vue developer", id: 3 },
      ],
    };
  },
};
</script>

<style></style>
