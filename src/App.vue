<template>
  <div id="app">
    <h1>Registro de Usuario</h1>
    <div>
      <label>Email:</label>
      <input type="email" v-model="email" />
    </div>
    <div>
      <label>Contraseña:</label>
      <input type="password" v-model="password" />
    </div>
    <button @click="handleRegister">Registrar</button>
    <p v-if="successMessage">{{ successMessage }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: '',
      successMessage: '',
    };
  },
  methods: {
    handleRegister() {
      // Aquí puedes agregar la lógica para enviar el correo y la contraseña a tu servidor o realizar la acción de registro.
      // Puedes usar servicios como Firebase, Axios, etc.

      // Simulación de éxito después de 2 segundos (¡reemplázalo con tu lógica real!)
      setTimeout(() => {
        this.successMessage = 'Usuario registrado con éxito';
      }, 2000);
    },
  },
};
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}

input {
  margin-bottom: 10px;
}

button {
  cursor: pointer;
  padding: 10px 20px;
  font-size: 16px;
}
</style>
