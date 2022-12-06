<template>
  <todo-list/>
  <task-list/>
</template>

<script>

import TodoList from "@/components/TodoList";
import TaskList from "@/components/TaskList";

export default {
  name:"App",

  components: {
    TodoList,
    TaskList
  }
}

</script>



