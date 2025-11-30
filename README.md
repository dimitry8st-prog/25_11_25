# Мой учебный проект по Git

## Cоздаю папку для проекта и захожу в нее:

bash
mkdir my-git-practice
cd my-git-practice

## Инициализирую Git-репозиторий:

bash
git init

# Шаг 2. Первый коммит ("затычка")
## Создаю главный файл проекта (нашу "затычку"):

bash
echo "# Мой учебный проект по Git" > README.md

## Проверяю статус репозитория:

bash
git status

## Добавляю файл в индекс (staging area):

bash
git add README.md

## Делаю первый коммит:

bash
git commit -m "Инициализация коммита: Добавление README.md"

# Шаг 3. Связывние с удаленным репозиторием
## Добавляю URL

bash
git remote add origin https://github.com/dimitry8st-prog/25_11_25.git

## Отправляю свои изменения в удаленный репозиторий (первый пуш):

bash 
git push -u origin main

