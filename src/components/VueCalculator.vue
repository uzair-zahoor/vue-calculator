<template>
  <!-- <h2>Hello from vue Calculator</h2> -->
  <div class="calc">
    <div class="view">
      <div class="input">
        <div class="record">{{ record }}</div>
        <input @keypress="show" @input="inputValue" v-model="calculatorvalue" />
      </div>
    </div>
    <div class="btns">
      <div class="btn-b" v-for="n in calculatorelement" :key="n">
        <div class="btn" @click="action(n)">
          {{ n }}
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "VueCal",
  data() {
    return {
      calculatorvalue: "",
      operator: null,
      previous: "",
      allPrevious: "",
      record: "",
      eqaul: "=",
      ans: "Ans",
      calculatorelement: [
        "C",
        "*",
        "/",
        "-",
        "7",
        "8",
        "9",
        "+",
        "4",
        "5",
        "6",
        "%",
        "1",
        "2",
        "3",
        "=",
        "0",
        ".",
      ],
    };
  },
  methods: {
    // input() {
    //   // if (!isNaN(this.calculatorvalue) || this.calculatorvalue === ".") {
    //   //   let a = (this.calculatorvalue += this.calculatorvalue + "");
    //   //   console.log(a);
    //   }
    show(e) {
      if (e.key == "Enter") {
        this.record = `${this.calculatorvalue} ${this.eqaul}`;
        this.calculatorvalue = `${this.ans} ${eval(this.calculatorvalue)}`;
        // console.log(this.calculatorvalue);
      }
    },
    action(v) {
      if (!isNaN(v) || v === ".") {
        this.calculatorvalue = "";
        this.calculatorvalue += v + "";
      }
      if (v === "C") {
        this.calculatorvalue = "";
        this.record = "";
      }
      if (v === "%") {
        this.calculatorvalue = this.calculatorvalue / 100;
      }
      if (["/", "*", "+", "-"].includes(v)) {
        this.operator = v;
        console.log(v);

        this.previous = this.calculatorvalue;
        this.calculatorvalue = "";
        // this.calculatorvalue = `${this.previous} ${this.operator}`;
      }
      if (v === "=") {
        this.record = `${this.previous} ${this.operator} ${this.calculatorvalue} ${v}`;
        this.calculatorvalue = `${this.ans} ${eval(
          this.previous + this.operator + this.calculatorvalue
        )}`;

        this.previous = "";
        this.operator = "";
      }
    },
  },
};
</script>
<style scoped>
.calc {
  width: 30%;
  margin: 20px auto;
  padding: 20px;
  /* border: 1px solid black; */
  box-shadow: 5px 5px 10px gray;
  background-color: rgb(31, 30, 44);
  border-radius: 10px;
}
.input {
  width: 90%;
  margin: auto;
  height: 60px;
  background-color: aliceblue;
  border-radius: 10px;
  border: none;
  outline: none;
  /* display: flex; */
  /* justify-content: flex-end; */
  /* align-items: center; */
  padding: 0px 10px;
  font-size: 22px;
  text-align: left;
}
.btn-b {
  display: inline-block;
}
.btns {
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-flow: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  padding: 30px 0px;
}
.btn {
  width: 80px;
  height: 60px;
  margin: 5px;
  background-color: aliceblue;
  border: 1px solid black;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 22px;
  border-radius: 10px;
  color: rgb(31, 30, 44);
}
input {
  width: 100%;
  height: 30px;
  padding-top: 5px;
  background-color: transparent;
  border: none;
  outline: none;
  font-size: 22px;
}
.record {
  margin-top: 5px;
  font-size: 18px;
}
@media screen and (max-width: 1100px) {
  .calc {
    width: 50%;
  }
}
</style>
