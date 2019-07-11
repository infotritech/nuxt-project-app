<template>
  <div class="text"
  :class="{fail: score < 50, good: score >= 80}">

    {{ score }}

    <h1 v-if="ok">{{age}} Hello {{name}}</h1>
    <h2 v-show="ok">{{upperName}}</h2>
    <div>{{ upperName }}</div>
    <input type="text" :value="name+'x'" />
    <br />
    <input type="text" v-model="name" />
    <br />
    <input type="text" v-model="name" />
    <br />
    <button @click="doSave">SAVE</button>
    <br />
    <button @click="doToggle">Toggle</button>
    <br />
    <h1>Student List</h1>
    <ul>
      <li v-for="st in student" :key="st.code">
        <span>{{ st.code }}</span>
        <span>{{ st.name }}</span>
      </li>
    </ul>
<!-- <div  -->
<!-- </div> -->

  </div>
  
</template>

<script>
export default {
  // data: function(){
  data() {
    //    setInterval(() => {
    //        this.name += '*'
    //    }, 3000);
    return {
      name: "World",
      age: 25,
      ok: true,

      student: [
        { code: '001', name: 'Name1' },
        { code: '002', name: 'Name2' },
        { code: '003', name: 'Name3' },
        { code: '003', name: 'Name4' },
      ],

      score: 50,
      
    };
  },
  computed: {
    upperName() {
      return this.name.toUpperCase();
    }
  },
  methods: {
    doSave() {
      console.log("SAVE");
    },
    doToggle() {
      this.ok = !this.ok;
    }
  }
};
</script>

