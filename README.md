# Контейнеризація додатку

## Кроки для виконання

### Контейнеризація беку
- Для початку створимо файл `docker-compose.prod.yml` та пропишемо його функціонал (код великий, тому краще скопіювати з файлу)
- Після, переходимо в `withlist-api`, далі нам потрібно змінити `Dockerfile` та `Dockerfile.dev` (у вас вони можуть збігатись, тому цей пункт опціональний)

### Контейнеризація фронту
- Почнемо зі створення `docker-compose.dev.yml` і пропишемо реалізацію (вона вказана у файлі)
- Переходимо в `wishlist-ui`, підготуємо `Dockerfile` для роботи з `nginx`
- В тій же директорії створюємо файл `nginx.conf` та прописуєм конфігурацію (вказана у файлі)

### Підняття додатку
- Для того щоб запустити додаток, виконаємо в консолі `docker-compose -f docker-compose.prod.yml up --build`</br> (для Linux: `sudo docker-compose -f docker-compose.prod.yml up --build`)
- Тепер переходимо в браузер та вписуємо в пошукову строку `localhost`

## Результати
* Відкриваємо сайт та реєструємось
  * <img width="890" height="650" alt="image" src="https://github.com/user-attachments/assets/dcea8d03-58e2-4b95-99b3-88c471df637f" /> </br>
* Після реєстрації (, для перевірки логіна, натискаємо <b>Logout</b>, та вводимо дані користувача, ) ми маємо можливість створити свій <b>Wishlist</b>, вводимо назву та натискаємо <b>Create</b>
  * <img width="890" height="650" alt="image" src="https://github.com/user-attachments/assets/7220684a-c1f5-4321-8348-6b4525a28253" />
  * <img width="890" height="650" alt="image" src="https://github.com/user-attachments/assets/7f8b0b38-c670-4d12-841d-a78f8044d64c" /> </br>
* Відкриваємо створений <b>Wishlist</b> та додаємо туди елементи:
  * <img width="890" height="650" alt="image" src="https://github.com/user-attachments/assets/3b9a075a-5ed2-4aa3-a775-0fe03c4a8dca" />
