# Prominado Guides: Битрикс24

## Директории для кастомизации
3 основных директории для работы с порталом:
/portal - директория для размещения всех кастомных страниц
/bitrix/php_interface/src - директория для размещения библиотек (и всего, что не имеет отношения к внешнему виду)
/bitrix/templates/bitrix24/custom - директория для размещения кастомных файлов шаблона

## Структура кастомных страниц
Все кастомные страницы должны лежать в директории "/portal".
1. Если необходимо создать страницу не имеющую отношения к коробочному функционалу (например: страницу отчетов), то можно создать произвольную структуру директорий (например: /portal/reports) и разместить ее там.
2. Если необходимо создать страницу имеющую отношение к коробочному функционалу (например: список счетов с привязкой к заказам), то следует разместить ее по пути: "/portal/crm/invoice/byorders"
3. Если необходимо добавить включаемую область для коробочной страницы (например: /crm/invoice/edit), необходимо разместить файл включаемой области по пути "/portal/crm/invoice/edit/viewcontent_%название_области%.php"
Если необходимо расширить функционал, не имеющий отношения к внешнему виду (например: добавить набор функций для работы со счетами), следует создать библиотеку, разместить ее тут: /bitrix/php_interface/src/invoice.php и подключить через composer по стандарту psr-4.

## Структура шаблона
Изменять шаблон bitrix24 стоит только в исключительных и крайних случаях, т.к. при обнолвении все изменеия будут утрачены. Содержимое следует изменять с помощью JS, а добавлять с помощью включаемях областей (в шаблоне их достаточное количество) или так же с помощью JS.
1. Для подключения сторонних файлов JS/CSS следует создать файл /bitrix/templates/bitrix24/custom/assets.php и подключить его в init.php
```
if(!CSite::InDir('/bitrix/')){
	function assetsInit(){
	    global $APPLICATION;
	    define('ASSETS_PATH', '/bitrix/templates/bitrix24/custom');
	    include_once($_SERVER['DOCUMENT_ROOT'].ASSETS_PATH.'/assets.php');
	}
	AddEventHandler("main", "OnPageStart", "assetsInit");
}
```
2. Размещать кастомные файлы шаблона следует в соответствующих директориях внутри /bitrix/templates/bitrix24/custom/
```
|bitrix24
|-_custom
| |-css
| | |-styles.css
| | |...
| |-js
| | |-scripts.js
| | |...
| |assets.php
| |...
|-components
|-images
|...
```