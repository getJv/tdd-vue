<template>
  <v-form @submit.prevent="$emit('submitted', username)">
    <v-text-field v-model="username" ></v-text-field>
    <v-btn type="submit">Enviar</v-btn>
  </v-form>
</template>
<script>
export default {

  data() {
    return {
      username: ''
    }
  }
}
</script>

