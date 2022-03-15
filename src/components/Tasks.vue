<template>
    <div :key="taskitem.id" v-for="taskitem in tasks">
        <Task :task="taskitem" />
    </div>
</template>


<script>
import Task from '@/components/Task';

export default {
    name: 'Tasks',
    props: {
        tasks: Array,
    },
    components: {
        Task,
    }
}
</script>
