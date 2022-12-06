<template>
  <ul>
    <li
        v-for="(task, index) in tasks"
        :key="task.id"
    >
      {{ index + 1 }}. {{ task.title }}
    </li>
  </ul>
</template>

<script>
import axios from 'axios';

export default {
  name: "TaskList",
  data() {
    return {
      tasks: []
    }
  },
  mounted() {
    axios
        .get('https://jsonplaceholder.typicode.com/todos')
        .then(response => {
          console.log(response)
          this.tasks = response.data;
        })
        .catch(error => console.log(error))
        .finally(() => console.log("Ok"))
  }
}
</script>

<style scoped>

</style>
