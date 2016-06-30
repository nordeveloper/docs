# Чеклист при разработке

> Тут находится все, что проверяем. Я потом в модуль все оформлю

## Контент
- Проверить, нет ли на сайте ссылок на dev‐сервер
- Проверить, не осталось ли на сайте тестового контента
- Проверить печатные версии страниц

## Стандарты и валидация
- [HTML Валидация](https://validator.w3.org/)
- [CSS Валидация](http://jigsaw.w3.org/css-validator/)
- В консоли JavaScript не выдает ошибок

## Тестирование функционала
- Проверить все формы на сайте
- Проверить сайт под админом и в инкогнито (если есть роли помимо администратор/пользователь - проверить под ними)
- Попробовать зарегистрироваться
- Попробовать восстановить пароль
- Проверить работу сайта в разных браузерах. [Стандарт поддержки браузеров — 2016 от Интерволги](http://www.intervolga.ru/blog/likbez/standart-podderzhki-brauzerov-2016/)
- Проверить все почтовые уведомления
- Проверить сайт с выключенным JavaScript
- Проверить везде ЧПУ
- Проверка schema.org
- [Проверка битых ссылок](https://validator.w3.org/checklink, http://iwebtool.com/broken_link_checker)

## Админка Битрикса
- Названия шаблонов
- Названия сайтов в админке
- Электронная почта в настройках сайта
- Учетная запись администратора клиента (и если сайт на поддержке - отдельная учетная запись для нас) с НОРМАЛЬНЫМИ паролями
- Настройки доступа у инфоблоков
- Проверить шаблоны путей до элементов инфоблоков в настройках инфоблоков
- Проверить галочки "Индексировать элементы" и "Индексировать разделы" в настройках инфоблоков
- Проверить все ли добавлено в исключения поиска /bitrix/admin/settings.php?mid=search
- Сгенерировать sitemap (/bitrix/admin/seo_sitemap.php?lang=ru)
- Добавить информацию о разработчике

## Безопасность
- Настроить бэкапы по расписанию (если сайт не на reg.ru)
- Проверить нет ли у посетителя доступа к служебным / закрытым разделам сайта
- Закрыть поисковикам доступ к служебным разделам в Robots.txt
- Отключить вывод ошибок на экран
- Проверить количество дискового пространства и на сколько его хватит
- Настроить запуски регулярных скриптов по крону
- Настроить email / sms уведомления о неработоспособности сайта


## Производительность
- [Оптимизировать картинки](https://compressor.io/)
- Проверить кэширование
- [Скорость сайта](https://developers.google.com/speed/pagespeed/)


## Финальные штрихи
- Favicon
- Robots.txt
- 404 страница
- Проверить заголовок, текст, картинку страниц при расшаривании в соцсетях
- Проверить иконки при добавлении сайта в избранное на мобильных устройствах
- [Мобильная версия](https://validator.w3.org/mobile/)
- Указать Viewport
- Заголовки и свойства страниц
- Счетчики
- Редирект www-nowww/nowww-www
- [Humans.txt](http://humanstxt.org/)