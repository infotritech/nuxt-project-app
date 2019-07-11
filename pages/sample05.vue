<template>
    <div>
        <h1 v-if="ok">{{age}} Hello {{name}} </h1>
        <h2 v-show="ok">{{upperName}}</h2>
        <div>{{ upperName }}</div>
        <input type="text" :value="name+'x'">
        <br>
        <input type="text" v-model="name">
        <br>
        <input type="text" v-model="name">
        <br>
        <button @click="doSave">SAVE</button>
        <br>
        <button @click="doToggle">Toggle</button>
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
           name: 'World',
           age: 25,
           ok: true,

       }
    },
    computed: {
        upperName() {
            return this.name.toUpperCase()
        },
    },
    methods: {
        doSave() {
        console.log('SAVE');
        },
        doToggle() {
            this.ok = !this.ok;
        },
    },
}
</script>

