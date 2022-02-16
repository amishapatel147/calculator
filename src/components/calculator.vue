<template>
  <div>
    <h1>simpple calculator</h1>
    <table border="1">
       
      <tr>
        <td colspan="2"><b>Enter First Number:</b></td>
        <td colspan="2"><input type="text" name="first" v-model="firstnumber" /></td>
      </tr>
      <tr>
        <td colspan="2"><b>Enter second Number:</b></td>
        <td colspan="2"><input type="text" name="second" v-model="secondnumber" /></td>
      </tr>
      <tr>
        <td>
          <button v-on:click="add()">Addition</button>
        </td>
        <td>
          <button v-on:click="sub()">Subtration</button>
        </td>
        <td>
          <button v-on:click="mul()">Multiply</button>
        </td>
        <td>
          <button v-on:click="div()">Division</button>
        </td>
      </tr>
      <tr>    
        <td colspan="4">
          <p>Ans:{{ ans }}</p>
        </td>
      </tr>
    </table>
  </div>
</template>


<script>
export default {
  name: "calculator",
  data() {
    return {
      ans: ' ',
      firstnumber: ' ',
      secondnumber: ' ',
    };
  },
  methods: {
    add() {
      this.ans = parseInt(this.firstnumber) + parseInt(this.secondnumber);
    },
    sub() {
      this.ans = parseInt(this.firstnumber) - parseInt(this.secondnumber);
    },
    mul() {
      this.ans = parseInt(this.firstnumber) * parseInt(this.secondnumber);
    },
    div() {
      this.ans = parseInt(this.firstnumber) / parseInt(this.secondnumber);
    },
  },
};
</script>
<style scoped>
div{
  width:50%;


  margin: 0 auto;
}
table{
  margin: 0 auto;

}
td{
  padding: 10px 20px;
}
</style>