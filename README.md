

# IF6WAS7 - Интернет-магазин одежды

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)
![SQLite](https://img.shields.io/badge/Database-SQLite-lightgrey.svg)

IF6WAS7 - интернет-магазин одежды на Flask с полным циклом онлайн-продаж. Проект включает товары на главной странице, систему оформления заказов, поиск товаров по названию.

![Главная страница IF6WAS7](https://ibb.co/0Rs048zp)

---

## 🚀 Быстрый старт

### Предварительные требования

- Python 3.8 или выше
- Установленный pip

### Установка и запуск

1. Клонируйте репозиторий
bash
git clone https://github.com/Artur1161/if6was7.git
cd if6was7

1. Создайте и активируйте виртуальное окружение

bash
python -m venv venv
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

1. Установите зависимости

bash
pip install -r requirements.txt

1. Запустите приложение

bash
python app.py

Приложение будет доступно по адресу: http://localhost:5000

---

✨ Функциональность

🛍 Покупательская зона

· Главная страница - каталог товаров
· Поиск товаров - поиск по названию
· Оформление заказа - форма с контактными данными
· Контакты - для связи
· О нас - история бренда
· Вход и регистрация

⚙️ Технические особенности


· Адаптивный дизайн (ПК)
· SQLite база данных с резервным копированием
· Подготовка к HTTPS/SSL

---

📁 Структура проекта

if6was7/
├── app.py                 # Основное приложение Flask
├── database.db            # База данных SQLite (создается автоматически)
├── proba.py               # проба
├── README.md              # вы тут
│
├── static/               # Статические файлы
│   ├── 3b.jpg       #1 картинка
│   └── style.css               # базовый ксс файл для стиля всех страниц
│
└── templates/                  # HTML шаблоны
    ├── about.html              # Страница "О нас"
    ├── base.html               # Главная
    ├── contact.html            # Контакты
    ├── index.html              # Главная
    ├── login.html              # Вход
    ├── order.html              # Оформление заказа
    ├── proba.html              # Проба
    ├── product.html            # Карточка товара
    ├── search.html             # Поиск товаров
    └── shop.html               # Страница магазина товаров

 
---

🛠 Технологический стек

Бэкенд:

· Python 3.8+
· Flask 2.0+
· Flask-Session
· SQLite3

Фронтенд:

· HTML CSS
· Jinja2 шаблоны

База данных:

· SQLite с моделями:
  · Товары (название, описание, цена, бренд, изображение)

---

Для добавления товаров используйте Flask shell или прямое редактирование базы данных. Пример добавления товара:

python
from app import app, db, Product
with app.app_context():
    new_product = Product(
        name="Balenciaga 3b",
        description="Штаны редан",
        price=2999,
        image="3b.jpg"
    )
    db.session.add(new_product)
    db.session.commit()

---

🚀 Развертывание

Локальная разработка

bash
python app.py
`

Продакшен (рекомендации)

· Используйте WSGI сервер (Gunicorn)
· Настройте Nginx как reverse proxy
· Включите HTTPS с SSL сертификатом
· Регулярное резервное копирование database.db

---

🤝 Участие в разработке

Приветствуются contributions! Порядок действий:
1. Форкните репозиторий
2. Создайте feature branch (git checkout -b feature/AmazingFeature)
3. Зафиксируйте изменения (git commit -m 'Add AmazingFeature')
4. Запушьте ветку (git push origin feature/AmazingFeature)
5. Откройте Pull Request

---

📄 Лицензия

Распространяется под лицензией MIT. См. файл LICENSE для деталей.

---

👥 Контакты

Artur1161 на гитхабе
почта - art.dada1804@gmail.com 

Ссылка на проект: https://github.com/Artur1161/if6was7
