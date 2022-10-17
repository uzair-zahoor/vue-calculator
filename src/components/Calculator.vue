<!-- <template>
  <div class="calc">
    <div class="view">
      <input type="text" />
    </div>
    <div class="press">
      <div class="row"><button class="btn clr">Clear</button></div>
      <div class="row">
        <button class="btn" @click="enter(9)">9</button>
        <button class="btn" @click="enter(8)">8</button>
        <button class="btn" @click="enter(7)">7</button>
        <button class="btn" @click="enter(*)">*</button>
      </div>
      <div class="row">
        <button class="btn">6</button>
        <button class="btn">5</button>
        <button class="btn">4</button>
        <button class="btn">/</button>
      </div>
      <div class="row">
        <button class="btn">1</button>
        <button class="btn">2</button>
        <button class="btn">3</button>
        <button class="btn">+</button>
      </div>
      <div class="row">
        <button class="btn">0</button>
        <button class="btn">.</button>
        <button class="btn">=</button>
        <button class="btn">-</button>
      </div>
    </div>
  </div>
</template>
<script>
// let btns = document.querySelectorAll(".btn");
// document.querySelector("input").value = string;
// console.log(btns);
// Array.from(btns).forEach((btn) => {
//   btn.addEventListener("click", (e) => {
//     console.log(e.target.innerHTML);
//     // console.log(e.target.innerHTML);
//   });
// });

export default {
  name: "CalCulator",
  data() {
    return {
      string: "hello world",
    };
  },

  methods: {},
};
</script>
<style scoped>
.calc {
  width: 30%;
  margin: 20px auto;
  /* border: 1px solid black; */
  box-shadow: 5px 5px 10px gray;
  background-color: rgb(31, 30, 44);
  border-radius: 10px;
}
input {
  min-width: 310px;
  height: 100px;
  /* border: none; */
  margin-top: 10px;
  border-radius: 10px;
  border: none;
  outline: none;
}
.press {
  padding: 10px;
}
.btn {
  width: 70px;
  height: 60px;
  margin: 5px 5px;
  border-radius: 10px;
  font-size: 20px;
  border: none;
  outline: none;
}
.clr {
  width: 310px;
}
</style> -->
