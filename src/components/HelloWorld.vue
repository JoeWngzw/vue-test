<template>
    <div class="hello">
        <!--<h1>{{msg}}</h1>-->

        <input type="checkbox" :checked="qx" @click="chbox(qx)">全选
        <hr>
        <input :checked="ccbox" :value='ccbox' @click="inbox(ccbox,index)"  v-for="(n) in index" :key="n.index"  type="checkbox">

    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
        props: {
            msg: String
        },
        data() {
            return {
                index:[1,2,3,4,5],
                qx:'',
                ccbox:'',
                nn:1,
            }
        },
        methods: {
            chbox(qx){
                this.qx =!qx;
                this.ccbox = !qx;
                if(this.qx == true){
                    this.nn=this.index.length;
                }else{
                    this.nn=1;
                }
            },

            inbox(cc,n){

                if(cc){
                    this.nn++
                }else {
                    this.nn--;
                }
                if(this.nn==n.length){
                    this.qx=true;
                }else {
                    this.qx=false;
                }
            }
        }

    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
