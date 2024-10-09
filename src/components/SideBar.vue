<template>
  <aside
    id="sidebar"
    :class="{ hidden: !sidebarVisible, visible: sidebarVisible }"
  >
    <div class="logo">
      <img src="../assets/logo.svg" alt="#" />
      <h1>BankDash.</h1>
    </div>
    <ul class="list">
      <li>
        <a href="#"><img src="../assets/home 2.svg" alt="" /> Dashboard</a>
      </li>
      <li>
        <a href="#"
          ><img src="../assets/transfer 1.svg" alt="" /> Transactions</a
        >
      </li>
      <li>
        <a href="#"><img src="../assets/user 3 1.svg" alt="" /> Accounts</a>
      </li>
      <li>
        <a href="#"
          ><img src="../assets/econometrics 1.svg" alt="" /> Investments</a
        >
      </li>
      <li>
        <a href="#"
          ><img src="../assets/credit-card 1.svg" alt="" /> Credit Cards</a
        >
      </li>
      <li>
        <a href="#"><img src="../assets/loan 1.svg" alt="" /> Loans</a>
      </li>
      <li>
        <a href="#"><img src="../assets/service 1.svg" alt="" /> Services</a>
      </li>
      <li>
        <a href="#"
          ><img src="../assets/econometrics 1.svg" alt="" /> My Privileges</a
        >
      </li>
      <li>
        <a href="#" class="active"
          ><img src="../assets/settings solid 1.svg" alt="" /> Setting</a
        >
      </li>
    </ul>
  </aside>
</template>

<script>
export default {
  name: "SideBar",
  props: {
    sidebarVisible: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
#sidebar {
  grid-row: span 6 / span 6;
  border-right: 1px solid var(--border-color);
}

#sidebar .logo {
  display: flex;
  padding: 0px;
  align-items: center;
  justify-content: center;
  gap: 10px;
  margin-top: 13px;
}

#sidebar .logo h1 {
  font-family: Mont;
  font-size: 25px;
  font-weight: 900;
  line-height: 31.95px;
  color: var(--primary-color);
}

.list {
  width: 211px;
  height: 555px;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

.list li a {
  padding: 5px;
  display: flex;
  gap: 20px;
  font-family: Inter;
  font-size: 18px;
  font-weight: 500;
  line-height: 21.78px;
  color: var(--link-color);
  align-items: center;
  position: relative;
}

.list li a.active {
  color: var(--secondary-color);
}

.list li a.active::before {
  content: "";
  position: absolute;
  left: -35%;
  top: 50%;
  transform: translateY(-50%);
  width: 6px;
  height: 60px;
  background-color: var(--secondary-color);
  border-radius: 0px 10px 10px 0px;
}

/* Медиа-запрос для экранов шириной до 1024px */
@media (max-width: 1024px) {
  nav {
    justify-content: space-around; /* Распределение элементов навигации */
  }
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
  #sidebar .logo {
    margin-top: 50px; /* Отступ сверху для логотипа */
  }

  #sidebar.visible {
    display: block; /* Показываем боковую панель, если она видима */
    position: absolute; /* Абсолютное позиционирование */
    z-index: 1000; /* Уровень слоя */
    background-color: var(--white-color); /* Цвет фона боковой панели */
    height: 194vh; /* Высота на весь экран */
  }
}

/* Медиа-запрос для экранов шириной до 1440px */
@media (max-width: 1440px) {
  .container {
    width: 1110px; /* Ширина контейнера */
  }
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
  .container {
    width: 325px !important; /* Ширина контейнера */
  }
  header {
    height: 140px; /* Высота заголовка */
  }
  .info {
    display: none; /* Скрываем информацию */
  }
  nav {
    margin-bottom: 45px; /* Отступ снизу для навигации */
  }
  .menu {
    margin-bottom: 50px; /* Отступ снизу для меню */
    margin-left: 29px; /* Отступ слева для меню */
  }
  .search-inp-mobile {
    display: block; /* Показываем мобильное поле поиска */
    position: absolute; /* Абсолютное позиционирование */
    top: 8%; /* Положение сверху */
    left: 5%; /* Положение слева */
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
  #sidebar.visible {
    height: 179vh;
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
