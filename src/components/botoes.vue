<template>
  <div class="componente-1">
    <input type="button" value="AC" @click="click()"/>
    <input type="button" value="+" id="btnsoma" />
  </div>
  <div class="componente-2">
    <input type="button" value="7" />
    <input type="button" value="8" />
    <input type="button" value="9" />
    <input type="button" value="-" />
  </div>
  <div class="componente-3">
    <input type="button" value="4" />
    <input type="button" value="5" />
    <input type="button" value="6" />
    <input type="button" value="X" />
  </div>
  <div class="componente-4">
    <input type="button" value="1" />
    <input type="button" value="2" />
    <input type="button" value="3" />
    <input type="button" value="/" />
  </div>
  <div class="componente-5">
    <input type="button" value="0" />
    <input type="button" value="." />
    <input type="button" value="=" />
  </div>
</template>
<script>
export default {
  name: "botoes",
  methods: {
    click(){
        alert(`voce clicou no botao`)
    }
  },
};
</script>
<style>
.componente-1 {
  height: 50px;
  display: flex;
  justify-content: space-between;
  border: 1px solid white;
  padding: 10px 10px;
}
.componente-1 > input {
  width: 50px;
  height: 50px;
}
.componente-2 {
  display: flex;
  height: 50px;
  border: 1px solid white;
  justify-content: center;
  gap: 10px;
  padding: 10px 10px;
}
.componente-2 > input {
  width: 50px;
  height: 50px;
}
.componente-3 {
  display: flex;
  height: 50px;
  border: 1px solid white;
  justify-content: center;
  gap: 10px;
  padding: 10px 10px;
}
.componente-3 > input {
  width: 50px;
  height: 50px;
}
.componente-4 {
  display: flex;
  height: 50px;
  border: 1px solid white;
  justify-content: center;
  gap: 10px;
  padding: 10px 10px;
}
.componente-4 > input {
  width: 50px;
  height: 50px;
}
.componente-5 {
  display: flex;
  height: 50px;
  border: 1px solid white;
  justify-content: end;
  gap: 10px;
  padding: 10px 10px;
}
.componente-5 > input {
  width: 50px;
  height: 50px;
}
</style>