Завдання 1
Запит:
GET https://jsonplaceholder.typicode.com/posts

Результат перевірки:
- Статус-код: 200 OK
- Формат відповіді: JSON
- Кожен об’єкт містить поля userId, id, title, body.
<img width="1711" height="739" alt="image" src="https://github.com/user-attachments/assets/f83971da-b0ee-41d0-aaaf-2e22ccbf3630" />

Завдання 2
Запит:
GET https://jsonplaceholder.typicode.com/posts/1

Результат перевірки:
- Статус-код: 200 OK 
- Поля у відповіді присутні: userId, id, title, body 
<img width="1718" height="709" alt="image" src="https://github.com/user-attachments/assets/b99cabb3-ecca-4a4c-abac-ee61c5037430" />

Завдання 3
Запит:
POST https://jsonplaceholder.typicode.com/posts

Результат перевірки:
- Статус-код: 201 Created 
- Поле id присутнє 
- Відповідь у форматі JSON 
<img width="1726" height="574" alt="image" src="https://github.com/user-attachments/assets/581baab2-0958-4a4d-8541-6ed5835b5d18" />

Завдання 4
Запит:
PUT https://jsonplaceholder.typicode.com/posts/1

Результат перевірки:
- Статус-код: 200 OK 
- Дані у відповіді оновлені 
<img width="1704" height="665" alt="image" src="https://github.com/user-attachments/assets/2fbdb75e-9488-4c85-8525-cf8425fffb97" />

Завдання 5
Запит:
DELETE https://jsonplaceholder.typicode.com/posts/1

Результат перевірки:
- Статус-код: 200 OK або 204 No Content
- Тіло відповіді порожнє або мінімальне ✅
<img width="1725" height="530" alt="image" src="https://github.com/user-attachments/assets/859a8971-2a65-466d-8b4c-5cf6711f0a4e" />
