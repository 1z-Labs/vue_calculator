<script>
export default {}
</script>

<template>
  <div class="calculator">
    <form name="forms">
      <input type="text" name="output" readonly />
        <input type="button" class="clear" value="C" />
        <input type="button" class="operator" value="/" />
        <input type="button" value="1" />
        <input type="button" value="2" />
        <input type="button" value="3" />
        <input type="button" class="operator" value="*" />
        <input type="button" value="4" />
        <input type="button" value="5" />
        <input type="button" value="6" />
        <input type="button" class="operator" value="+" />
        <input type="button" value="7" />
        <input type="button" value="8" />
        <input type="button" value="9" />
        <input type="button" class="operator" value="-" />
        <input type="button" class="dot" value="." />
        <input type="button" value="0" />
        <input type="button" class="operator result" value="=" />
    </form>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.calculator {
  width: 287px; /* gap + 버튼 width를 계산한 값 */
  border: 1px solid #333;
  background-color: #ccc;
  padding: 5px;
}

.calculator form {
  display: grid;
  grid-template-columns: repeat(4, 65px); /* 4줄 */
  grid-auto-rows: 65px;
  grid-gap: 5px;
}

.calculator form input { /* 각 버튼들의 스타일 */
  border: 2px solid #333;
  cursor: pointer;
  font-size: 19px;
}

.calculator form input:hover {
  box-shadow: 1px 1px 2px #333;
}

/* 클리어 버튼의 색상 */
.calculator form .clear {
  background-color: #ed4848;
  grid-column: span 3;
}

/* 연산자 및 기호 버튼의 색상 */
.calculator form .operator {
  background-color: orange;
}

/* . 버튼의 색상 */
.calculator form .dot {
  background-color: green;
}

.calculator form input[type='text'] {
  grid-column: span 4;
  text-align: right;
  padding: 0 10px;
} 

.calculator form .result {
  grid-column: span 2;
}
</style>