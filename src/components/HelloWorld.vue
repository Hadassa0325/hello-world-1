<template>
  <h1> Tab name  </h1>
    
    <ul id="example-1" v-if = isDisplay>
      <li v-for="item in items" :key="item.message"> 
           {{ item.message }}</li>
           </ul>

           <div class="test">

    <div v-if = !isDisplay>

        <button v-on:click ="isDisplay = true">appuyer pour afficher</button>

    </div>

    <div v-if = isDisplay>

        <button v-on:click ="isDisplay = false">cacher</button>

    </div>

  </div>
</template>

<script>
var example = document.getElementById("example-1")
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
data () {
  return{ 
  items: [   
       { message: 'GOMA Claude Esther' }, 
       { message: 'GOMA Claude Esther'}
  ],
  isDisplay: false
}
},
methods: {
    show: function () {
      example.isDisplay = true;
    },
    hide: function () {
      example.isDisplay = false;
    },
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
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
