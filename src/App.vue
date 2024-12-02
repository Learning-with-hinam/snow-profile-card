<script setup>
import { ref } from 'vue'

const user = ref({
  id: 1,
  avatar: 'https://www.w3schools.com/w3images/team3.jpg',
  name: 'snow',
  jobTitle: 'Software Engineer',
  university: 'Industrial University',
})
</script>

<template>
  <div>
    <h2 style="text-align: center">User Profile Card</h2>

    <div class="card">
      <img :src="user.avatar" alt="avatar" style="width: 100%" />
      <h1>{{ user.name }}</h1>
      <p>{{ user.jobTitle }}</p>
      <p>{{ user.university }}</p>
      <div style="margin: 24px 0">
        <a href="#"><i class="fa fa-dribbble"></i></a>
        <a href="#"><i class="fa fa-twitter"></i></a>
        <a href="#"><i class="fa fa-linkedin"></i></a>
        <a href="#"><i class="fa fa-facebook"></i></a>
      </div>
      <p><button>Contact</button></p>
    </div>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
