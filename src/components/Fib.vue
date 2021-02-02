<template>
  <div class="main">
    <h1>{{ msg }}</h1>
    <button @click="next_fib_sequence();" class="button-color">Next Fibonacci Number</button>
    <div class = "fibVal"> {{ curFibVal[nthSequence] }}</div>
  </div>
</template>

<script>
export default {
  props: {
    msg: String,
  },

  data() {
    return { 
      curFibVal : [0, 1],
      nthSequence : 0
    }
  },

  methods: {
    next_fib_sequence: function() {

      if(this.nthSequence < 1){
        this.nthSequence+=1;
      }

      else{
        /*
        console.log("nthSequence" + this.nthSequence);
        console.log(this.curFibVal[this.nthSequence]);
        console.log(this.curFibVal[this.nthSequence-1]);
        */
        this.curFibVal.push(this.curFibVal[this.nthSequence-1] + this.curFibVal[this.nthSequence]);
        this.nthSequence+=1;
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

.fibVal {
    font-size: 5vw;
}

.button-color {
  background-color: RGB(122,122,122);
  color: #0000FF;
}
</style>
