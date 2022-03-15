<template>
    <div :key="taskitem.id" v-for="taskitem in tasks">
        <Task 
            @delete-task="$emit('delete-task', taskitem.id)"
            @toggle-reminder="$emit('toggle-reminder', taskitem.id)"
            :task="taskitem" 
        />
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
    },
    emits: ['delete-task', 'toggle-reminder'],
}
</script>
