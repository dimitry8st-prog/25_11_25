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

# Шаг 4. Внесение изменений и еще один пуш
## Добавляю новую функциональность ("затычка" №2):

bash
echo "console.log('Hello Git');" > script.js

## Коммичу новые изменения:

bash
git add script.js
git commit -m "feat: add базового script.js" 

## Отправляю изменения на GitHub (теперь можно без -u):

bash
git push

# Шаг 5. Работа с ветками (создание, пулл-реквест/мерж)
## Создаю новую ветку для добавления стилей:

bash
git checkout -b feature/add-styles

## Создаю файл стилей и коммичу в эту ветку::

bash

echo "body { font-family: Arial; }" > style.css
git add style.css
git commit -m "feat: add basic CSS styles"

## Пушим новую ветку на GitHub:

bash
git push -u origin feature/add-styles

## Имитирую Пулл-Реквест (Merge Pull Request):

git checkout main
git pull origin feature/add-styles # "Стягиваю" изменения из ветки в main

### Или, что более корректно для Git:
git merge feature/add-styles

# Шаг 6: Получение изменений (Pull)

## Имитирую изменения на GitHub: Можно через веб-интерфейс отредактировать README.md, добавив строчку ## Внесено через GitHub.

## Локально "стягиваю" эти изменения:
bash
git pull origin main
