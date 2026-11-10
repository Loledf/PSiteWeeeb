PSiteWeb — управление сайтом через JSON

1. Редактируйте карточки в папках channels, article и services.
2. Чтобы добавить карточку, создайте новый JSON, например article3.json, и добавьте "article3.json" в массив article файла image/content.json.
3. В каждом JSON: category (channels/article/services), title, description, link, enabled. enabled=false скрывает карточку.
4. Настройки темы, фона и названия страницы — image/settings.json. Положите изображение image/photo.jpg при необходимости.
5. Загрузите ВСЮ распакованную папку на статический веб-хостинг. Открытие index.html напрямую с диска (file://) может блокировать чтение JSON. Для локального просмотра запустите в папке PSiteWeb: python -m http.server 8000 и откройте http://localhost:8000
6. Страница проверяет обновления JSON каждые 15 секунд при открытой вкладке. Изменения должны быть сохранены на сервере; ZIP сам по себе не является сервером.
7. Для статьи вставьте реальную ссылку вместо демонстрационной https://telegra.ph.
