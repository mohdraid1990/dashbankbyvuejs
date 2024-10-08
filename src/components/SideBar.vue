vue
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
  name: "SideBar", // Имя компонента
  props: {
    sidebarVisible: {
      // Свойство для управления видимостью боковой панели
      type: Boolean, // Тип свойства - логический
      default: false, // Значение по умолчанию - скрыто
    },
  },
};
</script>

<style lang="scss" scoped>
#sidebar {
  grid-row: span 6 / span 6; // Занимает 6 строк
  border-right: 1px solid var(--border-color); // Правая граница

  .logo {
    display: flex; // Используем flexbox
    padding: 20px; // Отступы
    align-items: center; // Выравнивание по центру
    justify-content: center; // Выравнивание по центру
    gap: 10px; // Промежуток между элементами
    margin-top: 28px; // Отступ сверху
  }

  .logo h1 {
    font-family: Mont; // Шрифт для заголовка
    font-size: 25px; // Размер шрифта
    font-weight: 900; // Жирность шрифта
    line-height: 31.95px; // Высота строки
    color: var(--primary-color); // Цвет заголовка
  }

  .list {
    width: 211px; // Ширина списка
    height: 555px; // Высота списка
    display: flex; // Используем flexbox
    flex-wrap: wrap; // Перенос элементов
    align-items: center; // Выравнивание по центру

    li a {
      padding: 5px; // Отступы для ссылок
      display: flex; // Используем flexbox
      gap: 20px; // Промежуток между элементами
      font-family: Inter; // Шрифт для ссылок
      font-size: 18px; // Размер шрифта
      font-weight: 500; // Жирность шрифта
      line-height: 21.78px; // Высота строки
      color: var(--link-color); // Цвет ссылок
      align-items: center; // Выравнивание по центру
      position: relative; // Относительное позиционирование

      &.active {
        color: var(--secondary-color); // Цвет активной ссылки
      }

      &.active::before {
        content: ""; // Псевдоэлемент для активной ссылки
        position: absolute; // Абсолютное позиционирование
        left: -35%; // Положение слева
        top: 50%; // Положение сверху
        transform: translateY(-50%); // Центрирование по вертикали
        width: 6px; // Ширина псевдоэлемента
        height: 60px; // Высота псевдоэлемента
        background-color: var(--secondary-color); // Цвет псевдоэлемента
        border-radius: 0px 10px 10px 0px; // Скругление углов
      }
    }
  }

  // Медиа-запрос для экранов шириной до 1024px
  @media (max-width: 1024px) {
    .logo h1 {
      font-size: 20px !important; // Размер шрифта для логотипа
    }

    .list {
      margin-top: 5px !important; // Отступ сверху для списка
    }

    .list li a {
      font-size: 15px !important; // Размер шрифта для ссылок в списке
    }

    #closeIcon {
      left: 60px; // Положение иконки закрытия
    }

    &.hidden {
      display: none; // Скрываем боковую панель
    }

    &.visible {
      display: block; // Показываем боковую панель, если она видима
      position: absolute; // Абсолютное позиционирование
      z-index: 1000; // Уровень слоя
      background-color: var(--white-color); // Цвет фона боковой панели
      height: 100%; // Высота на весь экран
    }
  }

  // Медиа-запрос для экранов шириной до 425px
  @media (max-width: 450px) {
    .list {
      margin-top: 10px; // Отступ сверху для списка
    }

    .list li a {
      font-size: 15px; // Размер шрифта для ссылок в списке
    }

    .info-mobile {
      display: block; // Показываем мобильную информацию
    }

    .name input,
    .name select {
      width: 280px; // Ширина полей ввода и выбора
      height: 40px; // Высота полей ввода и выбора
    }

    .link-main a {
      font-family: Inter; // Шрифт для ссылок
      font-size: 13px; // Размер шрифта
      font-weight: 500; // Жирность шрифта
      line-height: 15.73px; // Высота строки
    }
  }
}
</style>
