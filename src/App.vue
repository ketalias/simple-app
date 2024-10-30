<template>
  <nav>
    <router-link to="/">{{ $t("menu.home") }}</router-link>
    <router-link to="/">{{ $t("menu.contacts") }}</router-link>
  </nav>
  <div>
    <div class="box">
      <h1>Language: {{ $i18n.locale }}</h1>
      <button @click="changeL('en')">EN</button>
      <button @click="changeL('ua')">UA</button>
    </div>
    <div class="box">
      <h1>{{ $t("menu.home") }}</h1>
      <button @click="login">{{ $t("actionTitles.login") }}</button>
      <button @click="logout">{{ $t("actionTitles.logout") }}</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    changeL(lang) {
      this.$i18n.locale = lang;
    },
  },
};
</script>

<style lang="css" scoped>
.box {
}

nav {
  display: flex;
  justify-content: center;
  gap: 20px;
  background-color: #3498db;
  padding: 15px;
  border-radius: 8px;
}

nav a {
  color: white;
  font-size: 1.2rem;
  text-decoration: none;
  padding: 10px 15px;
  border-radius: 5px;
  transition: background-color 0.3s;
}

nav a:hover {
  background-color: #2980b9;
}

button {
  margin: 5px;
  padding: 10px 15px;
  border: none;
  background-color: #3498db;
  color: white;
  border-radius: 5px;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #2980b9;
}
</style>
