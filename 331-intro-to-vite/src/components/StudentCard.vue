<!-- <script setup lang="ts">
 import {ref} from 'vue'
// defineProps<{
//   msg: string
// }>()
const student = ref({
  "id": 1,
  "studentId": "SE-001",
  "name": "Prayuth",
  "surname": "The minister",
  "gpa": 3.59,
  "image": "https://firebasestorage.googleapis.com/v0/b/publicimage-41deb.appspot.com/o/tu.jpg?alt=media&token=171d65d0-8e8d-45d2-81db-021836316e02",
  "penAmount": 15,
  "description": "The great man ever!!!!"
})
  </script>

<template>
    <div class="student-class">
        <div class="student-card">
      <h3>{{ student.name }}</h3>
      <p>{{ student.surname }}</p>
      <p>GPA: {{ student.gpa }}</p>
    </div>
    </div>
    
  </template>
  
  
  
  <style scoped>
  .student-card {
    padding: 20px;
    width: 250px;
    cursor: pointer;
    border: 1px solid #39495c;
    margin-bottom: 18px;
    box-sizing: border-box;
  }
  .student-card:hover {
    transform: scale(1.01);
    box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
  }
  </style> -->
  
<script setup lang="ts">
import { Event } from "@/types"
import { ref } from "vue"
defineProps<{
  event:Event
}>()

</script>

<template>
 <div class="event-class">
   <div class="event-card">
     <h2>{{ event.name }} {{ event.surname }}</h2>
     <span>GPA is : {{ event.gpa }}</span>
   </div>
 </div>

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
</style>