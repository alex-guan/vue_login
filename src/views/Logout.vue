
<template>
    <div>
注销<Button @click="login">注销</Button>
<route_com></route_com>
    </div>
</template>

<script>
import route_com from '../components/route'
    export default {
        components:{
            route_com
        },
    data(){
        return{
           
        }
    },
      methods:{
         async login(){
            const result = await this.$http.get("/logout").then(data=>data.data);
            this.$store.commit('me/changeLogin',{result})

          }
        },
        
}
</script>

<style lang="lcss" scoped>

</style>