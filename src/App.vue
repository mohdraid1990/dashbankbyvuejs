<template>
  <div id="app">
    <div class="layout">
      <SideBar />
      <Header />
      <ProfileForm />
    </div>
  </div>
</template>

<script>
import SideBar from "./components/SideBar.vue";
import Header from "./components/AppHeader.vue";
import ProfileForm from "./components/ProfileForm.vue";

export default {
  name: "App",
  components: {
    SideBar,
    Header,
    ProfileForm,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&family=Montserrat:wght@100..900&display=swap");

/* Main colors */
:root {
  --primary-color: #343c6a;
  --secondary-color: #1814f3;
  --background-color: #f5f7fa;
  --text-color: #8ba3cb;
  --border-color: #e6eff5;
  --link-color: #b1b1b1;
  --white-color: #ffffff;
  --place-holder-color: #718ebf;
}

/* Body styles */
body {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  height: 100vh;
  font-family: "Montserrat", "Inter", sans-serif;
  background-color: var(--background-color);
}
a {
  text-decoration: none;
}

ul {
  list-style: none;
}

.container {
  width: 1600px; /* Ширина контейнера */
  margin: 0 auto; /* Центрирование контейнера */
}
.layout {
  display: grid; /* Используем сетку */
  grid-template-columns: repeat(12, 1fr); /* Определяем 12 колонок */
  gap: 0px; /* Устанавливаем промежутки между элементами */
}

.container {
  width: 1600px; /* Width of the container */
  margin: 0 auto; /* Center the container */
}
@media (max-width: 1024px) {
  .container {
    width: 650px !important; /* Ширина контейнера */
  }
}
@media (max-width: 1440px) {
  .container {
    width: 1110px; /* Ширина контейнера */
  }
}
@media (max-width: 450px) {
  .container {
    width: 325px !important; /* Ширина контейнера */
  }
}
</style>
