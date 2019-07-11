<template>
    <div>
        <h1>{{age}} Hello {{name}} </h1>
        <input type="text" :value="name+'x'">
    </div>
</template>

<script>
export default {
    // data: function(){
   data(){
       setInterval(() => {
           this.name += '*'
       }, 1000);
       return {
           name: 'Damrong',
           age: 25,

       }
    },
}
</script>

