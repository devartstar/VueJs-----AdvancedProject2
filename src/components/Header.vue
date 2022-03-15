<template>
    <header>
        <h1>{{ title }}</h1>
        <Button 
            :color="(showAddTask ? 'red' : 'green')" 
            :text="(showAddTask ? 'Close' : 'Add Task')" 
            @btn-click="$emit('toggle-add-task')"
        />
        <!-- <Button text="Done Task" color="green" />
        <Button text="Delete Task" color="red" /> -->
    </header>
</template>

<script>
import Button from '@/components/Button';
export default {
    name: 'Header',
    props: {
        title: {
            type: String,
            default: 'Task Manager'
        },
        showAddTask: Boolean
    },
    components: {
        Button
    },
}
</script>

<style scoped>
    header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    }
</style>