<template>
  <header>
    <div class="menu" id="menuIcon" @click="toggleSidebar">
      <img src="../assets/menu.svg" alt="Menu" />
    </div>
    <div
      class="menu close"
      id="closeIcon"
      v-if="sidebarVisible"
      @click="toggleSidebar"
    >
      <img src="../assets/close.svg" alt="Close" />
    </div>
    <div class="container">
      <nav>
        <div class="setting">
          <p>Setting</p>
        </div>
        <div class="info">
          <div class="search-inp">
            <img src="../assets/magnifying-glass 1.svg" alt="#input" />
            <input type="search" placeholder="Search for something" />
          </div>
          <div class="setting-info">
            <img src="../assets/settings 1.svg" alt="#" />
          </div>
          <div class="setting-info">
            <img src="../assets/002-notification-1.svg" alt="#" />
          </div>
          <div class="setting-info">
            <img
              src="../assets/pexels-christina-morillo-1181690 1.svg"
              alt="#"
            />
          </div>
        </div>
        <div class="search-inp-mobile" v-if="!sidebarVisible">
          <img src="../assets/magnifying-glass 1.svg" alt="#input" />
          <input type="search" placeholder="Search for something" />
        </div>
        <div class="info-mobile">
          <img src="../assets/pexels-christina-morillo-1181690 1.svg" alt="#" />
        </div>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      sidebarVisible: false,
    };
  },
  methods: {
    toggleSidebar() {
      this.sidebarVisible = !this.sidebarVisible;
      const sidebar = document.getElementById("sidebar");
      sidebar.classList.toggle("visible", this.sidebarVisible);
      sidebar.classList.toggle("hidden", !this.sidebarVisible);
    },
  },
};
</script>

<style scoped>
header {
  grid-column: span 11 / span 11;
  background-color: var(--white-color);
  height: 100px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px;
  border-bottom: 1px solid #e6eff5;
}

nav {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 60px;
}

.setting p {
  font-family: Inter;
  font-size: 28px;
  font-weight: 600;
  line-height: 33.89px;
  color: var(--primary-color);
}

.info {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
}

.search-inp {
  position: relative;
  display: flex;
  justify-content: center;
  width: 255px;
  height: 50px;
  background-color: var(--background-color);
  border-radius: 40px;
  padding: 5px;
  align-items: center;
}

.search-inp img {
  margin-top: 3px;
  margin-left: 24px;
  width: 20px;
  height: 20px;
}

.search-inp input {
  border: none;
  outline: none;
  flex: 1;
  text-align: right;
  font-size: 16px;
  background: none;
  font-family: Inter;
  font-size: 15px;
  font-weight: 400;
  line-height: 18.15px;
  color: var(--text-color);
  width: 152px;
  height: 18px;
  text-align: center;
}

.search-inp input::placeholder {
  font-family: Inter;
  font-size: 15px;
  font-weight: 400;
  line-height: 18.15px;
  color: var(--text-color);
}

.setting-info {
  width: 50px;
  height: 50px;
  background-color: var(--background-color);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

.info .setting-info:last-child img {
  border-radius: 50%;
  width: 60px;
  height: 60px;
}

.menu {
  display: none;
}

.info-mobile {
  display: none;
}

.search-inp-mobile {
  display: none;
}

.info-mobile img {
  display: block;
}

#closeIcon img {
  width: 25px;
}

#menuIcon {
  cursor: pointer;
}

#sidebar.visible #closeIcon {
  display: block;
}

#closeIcon {
  display: block;
  cursor: pointer;
  position: absolute;
  z-index: 1000;
  top: 10px;
  left: 159px;
  transition: transform 0.5s ease;
}

#closeIcon.rotate {
  transform: rotate(180deg);
}

#menuIcon {
  cursor: pointer;
}

@keyframes slideIn {
  from {
    transform: translateX(-100%);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}

@keyframes slideOut {
  from {
    transform: translateX(0);
    opacity: 1;
  }
  to {
    transform: translateX(-100%);
    opacity: 0;
  }
}

#sidebar.visible {
  animation: slideIn 0.5s forwards;
}

#sidebar.hidden {
  animation: slideOut 0.5s forwards;
}

/* Медиа-запрос для экранов шириной до 1024px */
@media (max-width: 1024px) {
  form .img-form {
    left: 32%; /* Положение формы изображения */
    margin-top: 60px; /* Отступ сверху */
  }
  .form-group {
    padding: 0 !important; /* Убираем отступы у группы форм */
  }
  .btn {
    justify-content: center !important;

    align-items: center !important;

    width: auto;
    height: auto;
  }
  side-bar .logo h1 {
    font-size: 20px !important; /* Размер шрифта для логотипа */
  }
  .list {
    margin-top: 5px !important; /* Отступ сверху для списка */
  }
  .list li a {
    font-size: 15px !important; /* Размер шрифта для ссылок в списке */
  }
  .menu {
    display: block; /* Показываем меню */
    margin-left: 100px; /* Отступ слева */
    cursor: pointer; /* Указатель курсора */
    margin-top: 9px; /* Отступ сверху */
  }
  #closeIcon {
    left: 60px; /* Положение иконки закрытия */
  }
  side-bar {
    display: none; /* Скрываем боковую панель */
  }
  header {
    grid-column: span 12 / span 10; /* Заголовок занимает 10 колонок */
  }
  .setting {
    margin-left: 30px; /* Отступ слева для настроек */
  }
  #sidebar.hidden {
    display: none; /* Скрываем боковую панель, если она скрыта */
  }
  .list {
    width: 165px; /* Ширина списка */
    height: 555px; /* Высота списка */
    display: flex; /* Используем flexbox */
    flex-wrap: wrap; /* Перенос элементов */
    align-items: center; /* Выравнивание по центру */
    margin-top: 90px; /* Отступ сверху */
  }
  #sidebar.visible {
    display: block; /* Показываем боковую панель, если она видима */
    position: absolute; /* Абсолютное позиционирование */
    z-index: 1000; /* Уровень слоя */
    background-color: var(--white-color); /* Цвет фона боковой панели */
    height: 100%; /* Высота на весь экран */
  }
}

/* Медиа-запрос для экранов шириной до 1440px */
@media (max-width: 1440px) {
  header {
    padding: 0; /* Убираем отступы у заголовка */
  }

  .line {
    width: 550px; /* Ширина линии */
  }
  .btn {
    justify-content: flex-end;
    width: auto;
    height: auto;
  }
}

/* Медиа-запрос для экранов шириной до 425px */
@media (max-width: 450px) {
  .line {
    width: 285px; /* Ширина линии */
  }
  form .img-form {
    left: 20%; /* Положение формы изображения */
    margin-top: 18px; /* Отступ сверху */
  }
  header {
    height: 140px; /* Высота заголовка */
  }
  .info {
    display: none; /* Скрываем информацию */
  }
  nav {
    margin-bottom: 45px; /* Отступ снизу для навигации */
    justify-content: space-around;
  }
  .menu {
    margin-bottom: 50px; /* Отступ снизу для меню */
    margin-left: 36px; /* Отступ слева для меню */
  }
  .search-inp-mobile {
    display: block; /* Показываем мобильное поле поиска */
    position: absolute; /* Абсолютное позиционирование */
    top: 8%; /* Положение сверху */
    left: 5%; /* Положение слева */
  }
  #closeIcon {
    left: 130px; /* Положение иконки закрытия */
  }
  .search-inp-mobile input {
    width: 325px; /* Ширина поля ввода */
    height: 40px; /* Высота поля ввода */
    border: none; /* Убираем границу */
    outline: none; /* Убираем обводку */
    border-radius: 40px; /* Скругление углов */
    background-color: var(--background-color); /* Цвет фона поля ввода */
    display: flex; /* Используем flexbox */
    justify-content: center; /* Выравнивание по центру */
    padding: 5px; /* Отступы */
    align-items: center; /* Выравнивание по центру */
  }
  .search-inp-mobile img {
    margin-bottom: -33px; /* Отступ снизу для изображения */
    margin-left: 18px; /* Отступ слева для изображения */
    width: 16px; /* Ширина изображения */
    height: 16px; /* Высота изображения */
  }
  .search-inp-mobile input::placeholder {
    font-family: Inter; /* Шрифт для плейсхолдера */
    font-size: 13px; /* Размер шрифта */
    font-weight: 400; /* Жирность шрифта */
    line-height: 15.73px; /* Высота строки */
    color: var(--text-color); /* Цвет плейсхолдера */
    padding: 50px; /* Отступы */
  }
  .setting p {
    font-family: Inter; /* Шрифт для текста настроек */
    font-size: 20px; /* Размер шрифта */
    font-weight: 600; /* Жирность шрифта */
    line-height: 24.2px; /* Высота строки */
    text-align: center; /* Выравнивание текста по центру */
  }
  .info-mobile img {
    width: 35px; /* Ширина изображения мобильной информации */
    height: 35px; /* Высота изображения мобильной информации */
    border-radius: 50%; /* Скругление углов изображения */
  }
  .list {
    margin-top: 10px; /* Отступ сверху для списка */
  }
  .list li a {
    font-size: 15px; /* Размер шрифта для ссылок в списке */
  }
  .info-mobile {
    display: block; /* Показываем мобильную информацию */
  }
  .name input,
  .name select {
    width: 280px; /* Ширина полей ввода и выбора */
    height: 40px; /* Высота полей ввода и выбора */
  }
  .link-main a {
    font-family: Inter; /* Шрифт для ссылок */
    font-size: 13px; /* Размер шрифта */
    font-weight: 500; /* Жирность шрифта */
    line-height: 15.73px; /* Высота строки */
  }
  main .link-main {
    gap: 30px; /* Промежуток между элементами */
  }
  .btn {
    display: flex;
    padding-top: 30px;
    justify-content: center;
    align-items: center;
    width: auto; /* Ширина кнопки */
    height: auto; /* Высота кнопки */
  }
  .btn button {
    width: 285px; /* Ширина кнопки */
    height: 40px; /* Высота кнопки */
  }
}

/* Медиа-запрос для экранов шириной до 325px */
@media (max-width: 325px) {
  .search-inp-mobile input {
    width: 287px; /* Ширина поля ввода для мобильного поиска */
  }
  .btn {
    right: 0% !important; /* Положение кнопки */
  }
}
</style>
