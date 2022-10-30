<template>
    <div>
        <div style="width: 80%; margin: auto; display: flex; justify-content: center;">
            <router-link v-for="(link, index) in links" :key="index" class="anchorbtn" :class="{ active: (index === activeId) }" :to="link.to" exact>{{link.name}}</router-link>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['links'],
        data(){
            return {
                activeId: -1,
            }
        },
        methods:{
            toActive(index){
                console.log('Called!!')
                this.activeId = index
            }
        }
    }
</script>

<style>
.nuxt-link-active{
    background-color: aquamarine;
}
.anchorbtn{
    margin: 15px;
    text-decoration: none;
    padding: 5px 20px;
}
.anchorbtn:hover{
  background-color:darkgray;
  color: rgb(0, 0, 0);
}
.active{
    color:brown;
}
</style>
