<script setup lang="ts">
// defineProps<{
//   msg: string
// }>()
//import { ref } from "vue"
import { type Event } from '@/types'
defineProps<{
  event:Event
}>()
</script>

<template>
  <!-- <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vite.dev/" target="_blank" rel="noopener">Vite</a> +
       -->
      <!-- <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>. -->
      What's next?
    <!-- </h3>
  </div> -->
  <RouterLink class="event-link" :to="{ name: 'event-detail-view', params: { id: event.id } }">
    <div class="event-card">
      <h2>{{ event.title }}</h2>
      <span>@{{ event.time }} on {{ event.date }}</span>
    </div>
  </RouterLink>
</template>

<style scoped>
.event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
}
.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}

.event-link {
  text-decoration: none;
  color: #2c3e50;
}
</style>