<template>
  <div id="login">
    <h1>Bem-vindo(a)</h1>
    <h2>{{ this.nome }}</h2>
    <form>
      <section class="form-section">
        <label for="password">Senha:</label>
        <input id="password" type="password" required />
      </section>
    </form>
  </div>
</template>

<script>

export default {
  name: 'Home',
  computed: {
    nome () {
      return this.$route.query.nome.replace(/"/g, '')
    },
    nmprodam () {
      return this.$route.query.nm_prodam
    }
  }
}
</script>

<style lang="scss" scoped>
#login {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100%;
  height: 100vh;
}
</style>
