<script>
import ChildComp from './ChildComp.vue'

export default {
    components: {
        ChildComp
    },
    data() {
        return {
            msg: 'from parent'
        }
    }
}
</script>

<template>
    <ChildComp>This is some slot content! {{ this.msg }}</ChildComp>
</template>