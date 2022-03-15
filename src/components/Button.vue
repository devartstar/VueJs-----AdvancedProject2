<template>
    <button 
        class="btn" 
        :style="{background: color}"
        @click="onCLicking()"
    >{{ text }}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color: String,
    },
    methods: {
        onCLicking() {
            console.log("Clicked");
        }
    }
}
</script>