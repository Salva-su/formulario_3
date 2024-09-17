<template>
  <div id="app" class="form-container">
    <h2>Formulario</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Nombre:</label>
        <input
          type="text"
          id="name"
          v-model="formData.name"
          required
        />
      </div>

      <div class="form-group">
        <label for="age">Edad:</label>
        <input
          type="number"
          id="age"
          v-model="formData.age"
          required
        />
      </div>

      <div class="form-group">
        <label for="birthDate">Fecha de Nacimiento:</label>
        <input
          type="date"
          id="birthDate"
          v-model="formData.birthDate"
          required
        />
      </div>

      <div class="form-group">
        <label for="email">Correo Electrónico:</label>
        <input
          type="email"
          id="email"
          v-model="formData.email"
          required
        />
      </div>

      <div class="form-group">
        <label for="password">Contraseña:</label>
        <input
          type="password"
          id="password"
          v-model="formData.password"
          required
        />
      </div>

      <div class="form-group">
        <label for="country">País:</label>
        <input
          type="text"
          id="country"
          v-model="formData.country"
          required
        />
      </div>

      <div class="form-group">
        <label for="locality">Localidad:</label>
        <input
          type="text"
          id="locality"
          v-model="formData.locality"
          required
        />
      </div>

      <div class="form-group">
        <label for="message">Mensaje:</label>
        <textarea
          id="message"
          v-model="formData.message"
          required
        ></textarea>
      </div>

      <button type="submit">Enviar</button>
    </form>

    <div v-if="submitted">
      <p><strong>tu respuestas</strong></p>
      <p><strong>Nombre:</strong> {{ formData.name }}</p>
      <p><strong>Edad:</strong> {{ formData.age }}</p>
      <p><strong>Fecha de Nacimiento:</strong> {{ formData.birthDate }}</p>
      <p><strong>Email:</strong> {{ formData.email }}</p>
      <p><strong>País:</strong> {{ formData.country }}</p>
      <p><strong>Localidad:</strong> {{ formData.locality }}</p>
      <p><strong>Mensaje:</strong> {{ formData.message }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: '',
        age: '',
        birthDate: '',
        email: '',
        password: '',
        country: '',
        locality: '',
        message: ''
      },
      submitted: false
    };
  },
  methods: {
    submitForm() {
      this.submitted = true;
    
    }
  }
};
</script>

<style scoped>
.form-container {
  width: 300px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
}

.form-group {
  margin-bottom: 15px;
}

form label {
  display: block;
  margin-bottom: 5px;
}

form input,
form textarea {
  width: 100%;
  padding: 8px;
  box-sizing: border-box;
  border-radius: 5px;
  border: 1px solid #ccc;
}

button {
  padding: 10px 15px;
  background-color: #42b983;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #339966;
}

p {
  margin-top: 20px;
  font-size: 1.1em;
}
</style>
