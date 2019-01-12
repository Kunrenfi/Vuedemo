<template>
    <div class="demo2">
      <ul>
        <li v-for="(item,index) in lists"
             @click="choose(index)"
            :class="{active:index=={current}}"
             :key="index">
          {{item}}
        </li>
      </ul>
      <button type="button" @click="add()">tianjia</button>
      <ul>
        <li v-for="(item,index) in list2"
            :key="index">
          {{item}}
        </li>
      </ul>
    </div>
</template>

<script>
   export default {
     name:"demo2",
     data(){
       return{
         current:'',
         lists:[1,2,3,4,5,6,7,8,9],
         list2:[]

       }
     },
     methods:{
       choose(index){
         this.current=index

       },
       add(){
         this.list2.push(this.lists[this.current])
       }
     }


   }
</script>

<style scoped>
li.active{
background: green;
}
</style>
