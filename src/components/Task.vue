<template>
    <div class="task1">
        <h3>{{ task.text }}</h3>
        <p>{{ task.day }}</p>
    </div>
</template>

<script>
export default {
    name: 'Task',
    props: {
        task: Object
    },
}
</script>

<style scope>
.fas {
  color: red;
}
.task1 {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}
.task1.reminder {
  border-left: 5px solid green;
}
.task1 h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>