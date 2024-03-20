<script>
export default {
    data() {
        return {
            text: ''
        }
    },
    methods: {
        onInput(e) {
            this.text = e.target.value
            if (condition) {
                
            }
        }
    }
}
</script>

<template>
    <input v-model="text" placeholder="Type here">
    <p>{{ text }}</p>
</template>

