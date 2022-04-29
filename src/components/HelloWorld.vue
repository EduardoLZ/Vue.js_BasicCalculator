<template>
 
   <b-container class="bv-example-row">
  <b-row>
   
    <b-col style="background-color:black;">
      <b-col cols="12" >
     <p class="text-danger"> NUMERO1: {{numero}} -- NUMERO2: {{numero2}}</p>
   </b-col>
      <b-row>
        <b-col class="mt-2" cols="3">
    <b-button @click="numero==0?numero=1:numero2=1" block variant="dark">1</b-button>
        </b-col>
        <b-col  cols="3">
      <b-button @click="numero==0?numero=2:numero2=2" class="mt-2"  block variant="dark">2</b-button>
        </b-col>
        <b-col cols="3">
         <b-button @click="numero==0?numero=3:numero2=3" class="mt-2"  block variant="dark">3</b-button>
        </b-col>
        <b-col cols="3">
        <b-button @click="op='+'" class="mt-2"  block variant="warning">+</b-button>
        </b-col>
         <b-col class="mt-2" cols="3">
    <b-button @click="numero==0?numero=4:numero2=4" block variant="dark">4</b-button>
        </b-col>
        <b-col  cols="3">
    <b-button @click="numero==0?numero=5:numero2=5" class="mt-2"  block variant="dark">5</b-button>
        </b-col>
        <b-col cols="3">
         <b-button @click="numero==0?numero=6:numero2=6" class="mt-2"  block variant="dark">6</b-button>
        </b-col>
        <b-col cols="3">
        <b-button @click="op='-'" class="mt-2"  block variant="danger">-</b-button>
        </b-col>
         <b-col class="mt-2" cols="3">
    <b-button @click="numero==0?numero=7:numero2=7" block variant="dark">7</b-button>
        </b-col>
        <b-col  cols="3">
    <b-button @click="numero==0?numero=8:numero2=8" class="mt-2"  block variant="dark">8</b-button>
        </b-col>
        <b-col cols="3">
         <b-button @click="numero==0?numero=9:numero2=9" class="mt-2"  block variant="dark">9</b-button>
        </b-col>
        <b-col cols="3">
        <b-button @click="op='*'" class="mt-2"  block variant="secondary">*</b-button>
        </b-col>
        
      <b-col cols="5" class="mb-2">
        <b-button @click="operacion" class="mt-2"  block variant="primary">=</b-button>
        </b-col>
       <b-col cols="4" class="mb-2">
        <b-button @click="limpiar" class="mt-2"  block variant="primary">Clean</b-button>
        </b-col>
        
        <b-col cols="3">
        <b-button @click="op='/'" class="mt-2"  block variant="success">/</b-button>
        </b-col>

       
      </b-row>
    </b-col>
    <b-col>

      <b-row>
        <b-col cols="12">
          RESULTADO:
        </b-col>
        <b-col>
            {{resultado}}
        </b-col>
      </b-row>
    </b-col>
    
  </b-row>
</b-container>
  
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      resultado:0, 
      op:'', 
      numero:0,
      numero2:0
    }
  },
  methods: {
    operacion(){
      if (this.op=='+') {
        this.resultado= this.numero+this.numero2
      }
      if (this.op=='-') {
        this.resultado= this.numero-this.numero2
      }
      if (this.op=='*') {
        this.resultado= this.numero*this.numero2
      }
      if (this.op=='/') {
        this.resultado= this.numero/this.numero2
      }
    },
    limpiar(){
      this.resultado=0
      this.numero=0
      this.numero2=0
    }
  
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
