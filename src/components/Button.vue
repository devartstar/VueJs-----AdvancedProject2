<template>
    <button 
        class="btn" 
        :style="{background: color}"
        @click="onClicking()"
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
        onClicking() {
            this.$emit('btn-click')
        }
    }
}
</script>