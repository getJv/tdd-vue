<template>
  <form @submit.prevent="$emit('submitted', username)">
    <input type="text" v-model="username" />
    <button type="submit">Enviar</button>
  </form>
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

