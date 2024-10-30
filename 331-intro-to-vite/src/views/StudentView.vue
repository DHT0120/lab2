<script setup lang="ts">
  import { ref, onMounted } from 'vue';
  import StudentService from '@/services/StudentService.ts';
  import StudentCard from '@/components/StudentCard.vue';
  import type { Event } from '@/types.ts'

//   const students = ref(null);
  
//   onMounted(() => {
//     fetchStudents().then(data => {
//       students.value = data;
//     });
//   });
const events = ref<Event[]>([])
onMounted(() => {
  StudentService.getEvents()
    .then((response) => {
      events.value = response.data
    })
    .catch((error) => {
      console.error('There was an error!', error)
    })
})
  </script>


<template>
    
      <h1 style="text-align: center;">Students Information</h1>
      <div class="events">
        <StudentCard v-for="event in events" :key="event.id" :event="event" />
      </div>
    
  </template>
  
  <style scoped>
  .events {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  </style>