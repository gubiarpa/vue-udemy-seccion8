<template>
  <form>
    <input
      type="text"
      class="form-control my-2"
      placeholder="Ingrese nombre"
      v-model="tarea.nombre"
      >
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
      <hr>
      {{tarea}}
  </form>
</template>

<script>
export default {
  name: 'Home',
  components: {
  },
  data() {
    return {
      tarea: {
        nombre: [],
        categorias: []
      }
    }
  },
}
</script>
