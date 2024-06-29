<template lang="">
    <div>
        <img alt="Vue logo" src="../assets/images/meow2.jpg" width="300" height="300">
        Test.vue 저자:{{name}}
        <div id="index" v-for="(item,index) in guest" :key="index">
        N: {{ index }} &nbsp;
        {{ item.name }} &nbsp;
        age: {{ item.age }} &nbsp;
        name: {{ item.title }} <hr>
  </div>
</div>
</template>
<script>
export default {
    name:'BoardTest',
    data(){
        return{
            name : 'meow coco',
            guest:[
            {name:'meow',age:3,title:'coco'},
            {name:'meooow',age:6,title:'장군이'},
            {name:'냥',age:7,title:'juhaneeee'}
            ],
        }
    }
    
}
</script>
<style lang="">
    
</style>