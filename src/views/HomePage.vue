<template>
  <ion-page>
    <ion-header>
     <ion-toolbar color="dark">
      <ion-title>Ejercicios Basicos</ion-title>
     </ion-toolbar>
   </ion-header>
 <ion-content>
      <h1>las cuatro operaciones </h1>
      <ion-item>
        <p>suma:{{a+b}}</p>
        <p>resta:{{a-b}}</p>
        <p>multiplicacion:{{a*b}}</p>
        <p>division:{{a/b}}</p>
      </ion-item>
      <ion-item>
        <ion-input label="Ingrese a:"placeholder="ingrese un numero" type="number" v-model.number="a"/>
        <ion-input label="Ingrese b:"placeholder="ingrese otro numero" type="number" v-model.number="b"/>
      </ion-item>
      <ion-item>
        <ion-input label="Ingrese nombre:"placeholder="Ingrese un nombre" type="text" v-model.number="nombre"/>
        <ion-input label="Ingrese edad:"placeholder="Ingrese edad" type="number" v-model.number="edad"/>
        
      </ion-item>
      <ion-item>
        <ion-buttn color="danger" @click="AdicionarEst()">
          Adicionar estudiante
        </ion-button>
        <ion-button color="warning" @click="AddStudent">
          Adicionar estudiante
        </ion-buttonv-if="a === 0">
        <p>a diferentes de cero.</p>
      </ion-item>
      <ion-item v-if="b === 0">
         <p>b diferentes de cero.</p>
      </ion-item>
    </ion-content>
  </ion-page>
  <ion-item>
 </template>

<script setup lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
import { ref } from 'vue';

const a= ref(15);
const b=ref(3);
const estudiantes = ref ([
  {nombre:"Juan",edad:20},
  {nombre:"Maria",edad:22},
  {nombre:"Pedro",edad:19},
  )]
  const nombre = ref("");
  const edad = ref(0);
  const AddStudent =()=>{
    nombre: nombre.value,
    edad: edad.value,

  }
);
nombre.value ="";
edad.value =0;
}
function AdicionarEst()
  
}

</script>

<style scoped>
#container {
  text-align: center;
  
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  
  color: #8c8c8c;
  
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
