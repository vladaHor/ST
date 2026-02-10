# Частина A

## Крок 1

У терміналі виконана команда:
docker run -d --rm -p 7080:5000 gprestes/the-internet:v2.6.5

Дана команда запускає контейнер у фоновому режимі та пробросює порт 5000 контейнера на локальний порт 7080.

<img width="1088" height="583" alt="image" src="https://github.com/user-attachments/assets/052f3cea-0dc8-4859-ba89-3852dc27fcc9" />

## Крок 2

У браузері було відкрито адресу:
http://localhost:7080

Після відкриття сторінки зʼявився вебзастосунок The Internet зі списком доступних прикладів, що свідчить про успішний запуск контейнера.
<img width="1905" height="954" alt="image" src="https://github.com/user-attachments/assets/fa6a2e66-9516-423c-a953-93e4620d06eb" />

## Крок 3

У ручному режимі відкрито сторінки:

Form Authentication
<img width="1920" height="763" alt="image" src="https://github.com/user-attachments/assets/d333a379-8910-4824-a521-a1bed4877cca" />

Add/Remove Elements
<img width="1920" height="945" alt="image" src="https://github.com/user-attachments/assets/310819d8-d26d-4489-aa28-ae5c6247c417" />

# Частина B. Створення автотестів у Katalon Recorder
## Крок 1. Встановлення Katalon Recorder
<img width="1595" height="936" alt="image" src="https://github.com/user-attachments/assets/42ceaf5b-16e1-4edd-ba86-81b70c61b92b" />

## Крок 2. Створення тестового набору

У Katalon Recorder було створено Test Suite з назвою SmokeSuite

<img width="398" height="153" alt="image" src="https://github.com/user-attachments/assets/e4a3a7d0-00d4-4cd5-9dcb-8858347ef538" />

## Крок 3. Тест №1 — Успішний логін (Positive test)
Було:
- Відкрито сторінку Form Authentication.
- Ввести логін: tomsmith.
- Ввести пароль: SuperSecretPassword!.
- Натиснути кнопку Login.

Перевірки (Assertions):
- На сторінці відображається повідомлення “You logged into a secure area!”;
- присутня кнопка Logout;
- користувач знаходиться у secure area.
<img width="1552" height="515" alt="image" src="https://github.com/user-attachments/assets/73770d29-86fb-48f5-9a96-179fcc44a157" />

## Крок 4. Тест №2 — Невдалий логін (Negative test)
Було зроблено:
- Відкрити сторінку Form Authentication.
- Ввести коректний логін.
- Ввести неправильний пароль.
- Натиснути кнопку Login.

Перевірки (Assertions):
- зʼявляється повідомлення про помилку авторизації;
- доступ до secure area відсутній;
- кнопка Logout не відображається.

<img width="1509" height="707" alt="image" src="https://github.com/user-attachments/assets/114079ff-0ad5-421f-b40f-497421286887" />

## Крок 5. Тест №3 — Add / Remove Elements
Було виконано:
- Відкрити сторінку Add/Remove Elements.
- Натиснути кнопку Add Element три рази.
- Перевірити наявність трьох кнопок Delete.
<img width="1518" height="506" alt="image" src="https://github.com/user-attachments/assets/88f58a89-6cf4-4d2d-8252-96baa8a11abb" />

- Видалити один елемент.
- Перевірити, що залишилося дві кнопки Delete.
<img width="1559" height="553" alt="image" src="https://github.com/user-attachments/assets/e50f55fb-0944-4c3e-8af3-00afe290010b" />

Перевірки (Assertions):
- кількість кнопок Delete відповідає очікуваній;
- після видалення елемента кількість кнопок коректно зменшується.

