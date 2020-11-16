<template>
  <form @submit.prevent="procesarFormulario">
    <!-- Textbox -->
    <div class="mt-2">
      <input
        type="text"
        class="form-control my-2"
        placeholder="Ingrese nombre"
        v-model.trim="tarea.nombre"
        >
    </div>
    <!-- Checkbox -->
    <div class="mt-2">
      <!-- Javascript -->
      <div class="form-check form-check-inline">
        <input
          id="chk-1"
          value="js"
          v-model="tarea.categorias"
          type="checkbox"
          class="form-check-input">
        <label
          for="chk-1"
          class="form-check-label">
            Javascript
        </label>
      </div>
      <!-- Node.js -->
      <div class="form-check form-check-inline">
        <input
          id="chk-1"
          v-model="tarea.categorias"
          value="nd"
          type="checkbox"
          class="form-check-input">
        <label
          for="chk-1"
          class="form-check-label">
            Node.js
        </label>
      </div>
    </div>
    <!-- Radiobutton -->
    <div class="mt-2">
      <!-- Urgente -->
      <div class="form-check form-check-inline">
        <input
          type="radio"
          id="rd-1"
          value="urg"
          v-model="tarea.estado"
          class="form-check-input"
          >
        <label
          for="rd-1"
          class="form-check-label">
          Urgente
        </label>
      </div>
      <!-- Relax -->
      <div class="form-check form-check-inline">
        <input
          type="radio"
          id="rd-1"
          value="rel"
          v-model="tarea.estado"
          class="form-check-input"
          >
        <label
          for="rd-1"
          class="form-check-label">
          Relax
        </label>
      </div>
    </div>
    <!-- Number -->
    <div class="mt-2">
      <input
        type="number"
        class="form-control"
        v-model.number="tarea.numero"
        >
    </div>
    <!-- Button -->
    <button
      class="btn btn-dark mt-2 btn-block"
      type="submit"
      :disabled="isInvalidForm"
      >
      Procesar
    </button>
  </form>
</template>

<script>
import { reactive } from 'vue';
export default {
  name: 'Home',
  components: {
  },
  data() {
    return {
      tarea: {
        nombre: '',
        categorias: [],
        estado: '',
        numero: 0
      }
    }
  },
  computed: {
    isInvalidForm() {
      return (
        (this.tarea.nombre === '')
      );
    }
  },
  methods: {
    procesarFormulario() {
      console.log(this.tarea);
    }
  },
}
</script>
