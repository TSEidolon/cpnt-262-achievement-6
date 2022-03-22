<script setup>
  import {ref} from 'vue'
  import ChildVSlot from './components/ChildVSlot.vue'
  import ChildHeader from './components/ChildHeader.vue'
  const message = ref('Hello My Name is Edgar and welcome to my lazily styled page')
  const titleColor = ref('title')
  const awesome = ref(false)
  const counter = ref(0)


  function toggle () {
    counter.value++
    awesome.value = !awesome.value
  }

  const items = ref ([
    {id:1, name:"Derrick Rose"},
    {id:2, name: "Allen Iverson"},
    {id:3, name:"Kevin Durant"}
  ])

</script>


<template>
  <div>
    <div>
      <ChildHeader>

      </ChildHeader>
    </div>
    <div class="MainContainer">
      <h1 :class="titleColor"> {{message}} </h1>
      <p> Click this button to know more about me! (Times clicked: {{counter}} )</p>
      <ChildVSlot> 
        <!-- The <p> in ChildVSlot will output here -->
        Click Below 
      </ChildVSlot>


      <button @click="toggle"> Click me! </button>
      <div v-if="awesome">
        <h3> My favourite basketball players are:</h3>
        <ul>
          <li v-for="item in items" :key="item.id">
            {{item.name}}
          </li>
        </ul>

      </div>
      <div v-else>
        <h1> Reveal this information by clicking above! </h1>
      </div>
    

    </div>
  </div>
</template>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.title {
  color: blue
}

.MainContainer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

body {
  margin: 0;
  padding: 0;
}
</style>
