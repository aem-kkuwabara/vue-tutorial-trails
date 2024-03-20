<script>
export default {
    mounted() {
        this.$refs.pElementRef.textContent = 'hello world!'
    }
}
</script>

<template>
    <p ref="pElementRef">hello</p>
</template>