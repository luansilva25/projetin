<template>
  <div class="resultado">
    <p id="resul">{{num1}} {{operador}} {{num2}}</p>
  </div>
  <div class="componente-1">
    <input type="button" value="AC" id="reset" @click="reset()" />
    <input type="button" value="+" id="soma" @click="operadores('+')" />
  </div>
  <div class="componente-2">
    <input type="button" value="7" @click="numeros('7')" />
    <input type="button" value="8" @click="numeros('8')" />
    <input type="button" value="9" @click="numeros('9')" />
    <input type="button" value="-" @click="operadores('-')" />
  </div>
  <div class="componente-3">
    <input type="button" value="4" @click="numeros('4')" />
    <input type="button" value="5" @click="numeros('5')" />
    <input type="button" value="6" @click="numeros('6')" />
    <input type="button" value="X" @click="operadores('*')" />
  </div>
  <div class="componente-4">
    <input type="button" value="1" id="um" @click="numeros('1')" />
    <input type="button" value="2" @click="numeros('2')" />
    <input type="button" value="3" @click="numeros('3')" />
    <input type="button" value="/" @click="operadores('/')" />
  </div>
  <div class="componente-5">
    <input type="button" value="0" @click="numeros('0')" />
    <input type="button" value="." @click="ponto()"/>
    <input type="button" value="=" id="calcular" @click="resul()" />
  </div>
</template>
<script>
export default {
  name: "botoes",
  data() {
    return {
      num1: "",
      operador: "",
      num2: "",
      resultado: "",
    };
  },
  methods: {
    numeros(Num) {
      if (this.operador) {
        if(this.num2.length <= 10)
        this.num2 += Num;
      else{
        alert(`voce nao podera passar do limite`)
      }
      } else {
        if(this.num1.length <= 10){
          this.num1 += Num;
        }
        else{
          alert(`voce passou do limite`)
        }
      }
    },
    operadores(operador) {
      this.operador = operador;
    },
    resul() {
      if (this.operador === "+") {
        (this.resultado = Number(this.num1) + Number(this.num2))
      } else if (this.operador === "-") {
        this.resultado = Number(this.num1) - Number(this.num2);
      } else if (this.operador === "*") {
        this.resultado = Number(this.num1) * Number(this.num2)
      } else {
        this.resultado = Number(this.num1) / Number(this.num2);
      }
      this.num1 = this.resultado.toString();
      this.operador = ''
      this.num2 = ''
    },
    reset() {
        (this.resultado = ""),
        (this.num1 = ""),
        (this.num2 = ""),
        (this.operador = "")
    },
    ponto(){
      if(this.operador){
        if(!this.num2.includes('.')){
           this.num2 += '.'
        }
      }
      else{
        if(!this.num1.includes('.')){
          this.num1 += '.'
        }
      }
    }
  },
};
</script>
<style>
.resultado {
  height: 100px;
  display: flex;
  align-items: center;
  justify-content: end;
  border: 1px solid white;
}
#resul {
  color: cornflowerblue;
  font-size: 50px;
}
.componente-1 {
  height: 70px;
  display: flex;
  justify-content: space-between;
  padding: 10px 10px;
}
.componente-1 > input {
  width: 70px;
  height: 70px;
  color: cornflowerblue;
  font-size: 30px;
  border: none;
  background-color: black;
  border: 1px solid rgb(33, 33, 33);
}
.componente-2 {
  display: flex;
  height: 70px;
  justify-content: center;
  gap: 10px;
  padding: 10px 10px;
}
.componente-2 > input {
  width: 70px;
  height: 70px;
  color: cornflowerblue;
  font-size: 30px;
  background-color: black;
  border: 1px solid rgb(33, 33, 33);
}
.componente-3 {
  display: flex;
  height: 70px;

  justify-content: center;
  gap: 10px;
  padding: 10px 10px;
}
.componente-3 > input {
  width: 70px;
  height: 70px;
  color: cornflowerblue;
  font-size: 30px;
  background-color: black;
  border: 1px solid rgb(33, 33, 33);
}
.componente-4 {
  display: flex;
  height: 70px;
  justify-content: center;
  gap: 10px;
  padding: 10px 10px;
}
.componente-4 > input {
  width: 70px;
  height: 70px;
  color: cornflowerblue;
  font-size: 30px;
  background-color: black;
  border: 1px solid rgb(33, 33, 33);
}
.componente-5 {
  display: flex;
  height: 70px;
  justify-content: end;
  gap: 5px;
  padding: 10px 10px;
}
.componente-5 > input {
  background-color: black;
  width: 65px;
  height: 65px;
  color: cornflowerblue;
  font-size: 30px;
  border: 1px solid rgb(33, 33, 33);
}
#calcular {
  color: white;
  background-color: cornflowerblue;
}
</style>