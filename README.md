# python_autotests
Мои автотесты в питоне
Автотесты написаны Praded458.
## Описание проекта и задачи
Автоматизация часть проверок регистрации тренера, создание сущности, изменение имени, изменение состояния.
## Детали реализации
### Файл main.py содержит возможность регистрации, а также подтверждение емайл.
1. Регистрация: используется header токен и body из переменной и формат json post метод post(url = F'{URL}/trainers/reg'). Выводится сообщение ответа.
Подтверждение эл. почты: post(url = F'{URL}/trainers/confirm_email').
2. Создание сущности методом post(url=f'{URL}/pokemons', в переменных передаем header и body. Выводится сообщение о создании сущности и id.
3. Изменение пораметра name сущности метод put(url=f'{URL}/pokemons', в переменных передаем header и body (с новым именем). Выводится сообщение о создании сущности и id.
4. Изменение состояния сущности метод post(url=f'{URL}/trainers/add_pokeball', в переменных передаем header и body. Выводится сообщение о состояния сущности.
![image](https://github.com/praded458/python_autotests/blob/main/2024-07-09_10-57-43.png)
### Файл test_praded458.py содержит автотест, определяет статус get запроса.
1. Успешность статуса при сравнении равенства id сущности с переменной trainer_id.
2. Сравнение параметра name из полученного ответа с переменной pokemon_name.
3. Используется библиотека @pytest, с помощью ключей сравниваются с переменными такие параметры, как: [('name', POKEMON_NAME), ('trainer_id', TRAINER_ID), ('id', POKEMON_ID)].
![image](https://github.com/praded458/python_autotests/blob/main/2024-07-09_10-23-46.png)
### Локальный запуск в терминале.
1. Скачать проект и открыть в терминале.
2. Перейти в директорию проекта.
3. В терминале в папке с проектом main.py импорт библиотек import requests  команда pip install requests
4. В терминале в папке с проектом в файле замените токен юзера 'user_token' на свой
5. В терминале в папке с проектом test_praded458.py импорт библиотек import pytest и import requests команда pip install requests и pip install pytest

### 
Fвтор Сергей Авдеев
