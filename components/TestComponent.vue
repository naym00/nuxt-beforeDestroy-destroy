<template>
    <div>
        <h1>Test Component</h1>
    </div>
</template>

<script>
    export default {
        methods:{
            commonMethod(text){
                this.$emit('test', text)
            }
        },
        beforeDestroy() {
            this.commonMethod('Before Destroy')
        },
        destroyed() {
            this.commonMethod('Destroy')
        }
    }
</script>