<template>
  <div>
    <h1>Jobs</h1>
    <div v-for="job in jobs" :key="job.id" class="job">
      <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
        <h2>{{ job.title }}</h2>
      </router-link>
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

<style>
.job h2 {
  background: #f4f4f4;
  border-radius: 10px;
  cursor: pointer;
  color: #444;
  max-width: 600px;
  margin: 10px auto;
  padding: 20px;
}
.job h2:hover {
  background: #ddd;
}
.job a {
  text-decoration: none;
}
</style>
