<template>
    <div>
        <h1>主页</h1>
        <Button @click="getTest">敏感接口</Button>
        {{result}}
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
                result:""
            }
        },
        methods:{
         async getTest(){
             this.result = await this.$http.get("/").then(res=>res)
          }
        }
    }
</script>

<style lang="less" scoped>

</style>