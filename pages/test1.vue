<template>
    <div>
        <h1>Test 1</h1>
        <button type="button" @click="flag = !flag">click</button><br>
        {{lifeCycle}}
        <test-component v-if="flag" @test="gotit($event)"/>
    </div>
</template>

<script>
  import TestComponent from '../components/TestComponent'
    export default {
        components: {
        'test-component': TestComponent,
        },
        data(){
            return {
                flag: true,
                lifeCycle: []
            }
        },
        methods:{
            gotit(data){
                this.lifeCycle.push(data)
            }
        }
        
    }
</script>

<style lang="scss" scoped>

</style>