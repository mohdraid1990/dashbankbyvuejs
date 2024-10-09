<!-- src/components/ProfileForm.vue -->
<template>
  <main>
    <div class="container">
      <ul class="link-main">
        <!-- Основные ссылки -->
        <li><a href="#">Edit Profile</a></li>
        <!-- Редактировать профиль -->
        <li><a href="">Preferences</a></li>
        <!-- Настройки -->
        <li><a href="">Security</a></li>
        <!-- Безопасность -->
      </ul>
      <div class="line"></div>
      <form action="">
        <div class="img-form">
          <!-- Форма изображения -->
          <img
            src="../assets/pexels-christina-morillo-1181690-1-66ffca7ebdddb.webp"
            alt="#"
          />
          <div class="pen">
            <img src="../assets/pencil-alt 1.svg" alt="" />
          </div>
        </div>
        <div class="form-group">
          <!-- Группа форм -->
          <div class="left">
            <!-- Левая часть формы -->
            <div class="name">
              <label for="Name">Your Name</label>
              <input type="text" placeholder="Charlene Reed" />
              <!-- Имя -->
            </div>
            <div class="name">
              <label for="Email">Email</label>
              <input type="text" placeholder="charlenereed@gmail.com" />
              <!-- Электронная почта -->
            </div>
            <div class="name">
              <label for="dob">Date of Birth</label>
              <div class="select-container">
                <select id="dob">
                  <!-- Выбор даты рождения -->
                  <option value="" disabled selected>25 January 1990</option>
                  <option value="1990">1990</option>
                  <option value="1991">1991</option>
                  <option value="1992">1992</option>
                  <option value="1993">1993</option>
                  <option value="1994">1994</option>
                </select>
                <img
                  id="arrow-icon"
                  src="../assets/Vector 4.svg"
                  alt="Arrow Icon"
                />
                <!-- Иконка стрелки -->
              </div>
            </div>
            <div class="name">
              <label for="Address">Permanent Address</label>
              <input type="text" placeholder="San Jose, California, USA" />
              <!-- Постоянный адрес -->
            </div>
            <div class="name">
              <label for="PostalCode">Postal Code</label>
              <input type="text" placeholder="45962" />
              <!-- Почтовый индекс -->
            </div>
          </div>
          <div class="right">
            <!-- Правая часть формы -->
            <div class="name">
              <label for="UserName">User Name</label>
              <input type="text" placeholder="Charlene Reed" />
              <!-- Имя пользователя -->
            </div>
            <div class="name">
              <label for="Password">Password</label>
              <input type="password" placeholder="**********" />
              <!-- Пароль -->
            </div>
            <div class="name">
              <label for="PresentAddress">Present Address</label>
              <input type="text" placeholder="San Jose, California, USA" />
              <!-- Текущий адрес -->
            </div>
            <div class="name">
              <label for="City">City</label>
              <input type="text" placeholder="San Jose" />
              <!-- Город -->
            </div>
            <div class="name">
              <label for="Country">Country</label>
              <input type="text" placeholder="USA" />
              <!-- Страна -->
            </div>
          </div>
        </div>
      </form>
      <div class="btn">
        <button type="submit">Save</button>
        <!-- Кнопка сохранения -->
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "ProfileForm",
};
</script>

<style scoped lang="scss">
main {
  grid-column: span 11 / span 11;
  height: 717px;
  grid-column-start: 2;
  grid-row-start: 2;
  margin: 30px;
  border-radius: 25px;
  padding: 20px;
  width: 1110px;
  background-color: var(--white-color);
  /* Цвет фона основного контента */
}

main .link-main {
  display: flex;
  /* Используем flexbox */
  align-items: center;
  /* Выравнивание по центру */
  gap: 60px;
  /* Промежуток между элементами */
}

.link-main a {
  color: var(--primary-color);
  /* Цвет الرابط */
  font-family: Inter;
  /* Шрифт для ссылок */
  font-size: 16px;
  /* Размер шрифта */
  font-weight: 500;
  /* Жирность шрифта */
  line-height: 19.36px;
  /* Высота строки */
  position: relative;
  /* Позиционирование */
  transition: color 0.3s ease-in-out;
  /* Плавный переход цвета текста */
}

.link-main a:hover::before {
  content: "";
  /* Псевдоэлемент при наведении */
  height: 3px;
  /* Высота псевдоэлемента */
  width: 114px;
  /* Ширина псевдоэлемента */
  background-color: var(--secondary-color);
  /* Цвет псевдоэлемента при наведении */
  position: absolute;
  /* Абсолютное позиционирование */
  bottom: -17px;
  /* Положение снизу */
  left: -13px;
  /* Положение слева */
  transition: width 0.3s ease-in-out;
  /* Плавный переход ширины */
}

.line {
  width: 1050px;
  /* Ширина линии */
  height: 1px;
  /* Высота линии */
  background-color: #f4f5f7;
  /* Цвет линии */
  margin-left: 20px;
  /* Отступ слева */
}

form {
  display: flex;
  /* Используем flexbox */
  gap: 50px;
  /* Промежуток между элементами */
  flex-wrap: wrap;
  /* Перенос элементов */
}

form .img-form {
  position: relative;
  /* Относительное позиционирование */
  width: 130px;
  /* Ширина формы изображения */
  height: 130px;
  /* Высота формы изображения */
  margin-top: 50px;
  /* Отступ сверху */
  margin-left: 32px;
  /* Отступ слева */
}

form .img-form img {
  border-radius: 50%;
  /* Скругление углов изображения */
}

.pen {
  position: absolute;
  /* Абсолютное позиционирование */
  background-color: var(--secondary-color);
  /* Цвет фона */
  width: 30px;
  /* Ширина элемента */
  height: 30px;
  /* Высота элемента */
  border-radius: 50%;
  /* Скругление углов */
  display: flex;
  /* Используем flexbox */
  align-items: center;
  /* Выравнивание по центру */
  justify-content: center;
  /* Выравнивание по центру */
  top: 66%;
  /* Положение сверху */
  right: 0%;
  /* Положение справа */
  cursor: pointer;
  /* Указатель курсора */
}

.form-group {
  padding-top: 20px;
  /* Отступ сверху */
  display: flex;
  /* Используем flexbox */
  align-items: center;
  /* Выравнивание по центру */
  justify-content: center;
  /* Выравнивание по центру */
  flex-wrap: wrap;
  /* Перенос элементов */
  gap: 20px;
  /* Промежуток между элементами */
}

.name {
  display: flex;
  /* Используем flexbox */
  flex-direction: column;
  /* Вертикальная ориентация */
  gap: 10px;
  /* Промежуток между элементами */
}

.name label {
  font-family: Inter, sans-serif;
  /* Шрифт для меток */
  font-size: 16px;
  /* Размер шрифта */
  font-weight: 400;
  /* Жирность шрифта */
  line-height: 19.36px;
  /* Высота строки */
  color: #232323;
  /* Цвет текста */
  padding-top: 20px;
  /* Отступ сверху */
}

.name input,
.name select {
  width: 418px;
  /* Ширина полей ввода */
  height: 50px;
  /* Высота полей ввода */
  border-radius: 15px;
  /* Скругление углов */
  outline: none;
  /* Убираем обводку */
  appearance: none;
  /* Убираем стандартный стиль */
  padding-left: 10px;
  /* Отступ слева */
  border: 1px solid #dfeaf2;
  /* Граница */
}

.name input::placeholder {
  font-family: Inter, sans-serif;
  font-size: 15px;
  font-weight: 400;
  line-height: 18.15px;
  padding: 20px;
  color: var(--place-holder-color);
}

.select-container {
  position: relative;
  display: inline-block;
}

#dob {
  appearance: none;
  font-family: Inter, sans-serif;
  font-size: 15px;
  font-weight: 400;
  line-height: 18.15px;
  color: var(--place-holder-color);
  cursor: pointer;
  padding-left: 20px;
}

#arrow-icon {
  position: absolute;
  right: 30px;
  top: 50%;
  transform: translateY(-50%);
  transition: transform 0.3s ease;
  pointer-events: none;
}

.select-container:focus-within #arrow-icon {
  transform: translateY(-50%) rotate(180deg);
}

.select-container:not(:focus-within) #arrow-icon {
  transform: translateY(-50%) rotate(0deg);
}

.btn {
  display: flex;
  justify-content: center;
  margin-top: 26px;
  align-items: center;
  margin-right: 13px;
}

.btn button {
  width: 190px;
  height: 50px;
  background-color: var(--secondary-color);
  border: none;
  border-radius: 20px;
  color: var(--white-color);
  font-family: Inter;
  font-size: 18px;
  font-weight: 500;
  line-height: 21.78px;
  text-align: center;
  cursor: pointer;
}

/* Медиа-запрос для экранов шириной до 1024px */
@media (max-width: 1024px) {
  main {
    height: 100%;
    width: 715px;
  }

  form .img-form {
    left: 32%;
    /* Положение формы изображения */
    margin-top: 60px;
    /* Отступ сверху */
  }

  .form-group {
    padding: 0 !important;
    /* Убираем отступы у группы форм */
  }

  .btn {
    justify-content: center !important;

    align-items: center !important;

    width: auto;
    height: auto;
  }

  .line {
    width: 550px !important;
    margin-top: 15px;
  }
}

/* Медиа-запрос для экранов шириной до 1440px */
@media (max-width: 1440px) {
  .btn {
    justify-content: flex-end;
    width: auto;
    height: auto;
  }
}

/* Медиа-запрос для экранов шириной до 425px */
@media (max-width: 450px) {
  .container {
    width: 325px !important;
    /* Ширина контейнера */
  }

  main {
    grid-column: span 1 / span 1;
    /* Занимает 1 колонку */
    height: 100%;
    /* Высота на весь экран */
    grid-column-start: 2;
    /* Начало со 2 колонки */
    grid-row-start: 2;
    /* Начало со 2 строки */
    background-color: var(--white-color);
    /* Цвет фона основного контента */
    /* Отступы */
    border-radius: 10px;
    /* Скругление углов */
    /* Ширина основного контента */
    padding: 10px;
    /* Отступы */
    margin-top: 30px;
    /* Отступ сверху */
  }

  .line {
    width: 285px !important;
    /* Ширина линии */
    margin-top: -8px;
  }

  form .img-form {
    left: 20%;
    /* Положение формы изображения */
    margin-top: 18px;
    /* Отступ сверху */
  }

  .name input,
  .name select {
    width: 280px;
    /* Ширина полей ввода и выбора */
    height: 40px;
    /* Высота полей ввода и выбора */
  }

  .link-main a {
    font-family: Inter;
    /* Шрифт для ссылок */
    font-size: 13px;
    /* Размер шрифта */
    font-weight: 500;
    /* Жирность шрифта */
    line-height: 15.73px;
    /* Высота строки */
  }

  main .link-main {
    gap: 30px;
    /* Промежуток между элементами */
  }

  .btn {
    display: flex;
    padding-top: 30px;
    justify-content: center;
    align-items: center;
    width: auto;
    /* Ширина кнопки */
    height: auto;
    /* Высота кнопки */
  }

  .btn button {
    width: 285px;
    /* Ширина кнопки */
    height: 40px;
    /* Высота кнопки */
  }
}

@media (max-width: 450px) {
  main {
    width: 325px;
    margin: 30px 15px;
    border-radius: 15px;
  }
}
</style>
