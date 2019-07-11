<template>
    <div>
        <h1>{{age}} Hello {{name}} </h1>
        <h2>{{upperName}}</h2>
        <div>{{ upperName }}</div>
        <input type="text" :value="name+'x'">
        <br>
        <input type="text" v-model="name">
        <br>
        <input type="text" v-model="name">
    </div>
</template>

<script>
export default {
    // data: function(){
   data(){
    //    setInterval(() => {
    //        this.name += '*'
    //    }, 3000);
       return {
           name: 'Damrong',
           age: 25,

       }
    },
    computed: {
        upperName() {
            return this.name.toUpperCase()
        },
    },
}
</script>

