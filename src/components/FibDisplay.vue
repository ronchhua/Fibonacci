<template>
  <div class="fib-wrapper">
    <h1>{{ msg }}</h1>
    <button @click="nextFibSequence" class="button-color">Next Fibonacci Number</button>
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
    nextFibSequence: function() {

      if(this.nthSequence > 0){
        var nextFibNum = this.curFibVal[this.nthSequence-1] + this.curFibVal[this.nthSequence];
        this.curFibVal.push(nextFibNum);
      }
      this.nthSequence+=1;
    }
    
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.fibVal {
    font-size: 5vw;
}

.button-color {
  background-color: RGB(122,122,122);
  color: #0000FF;
}
</style>
