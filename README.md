![img](https://webdesignchannel.ru/wp-content/uploads/gulp.png)

Optimize Html framework - GULP PACK 
=====================================

Используйте эту сборку для ускоренной верстки сайтов.
Gulp pack - Включает в себя минификацию изображений, js, css, а также компиляцию из sass в сss. Все изменения автоматически отслеживаются браузером.


СТРУКТУРА ПРИЛОЖЕНИЯ
-------------------

      app/             Рабочая папка
      prod/            Папка для продакшена (по умолчанию не создана). Создается после выполнения команды gulp production
      package.json     Зависимости
      yarn.lock        Служебный файл для проверки целостности
      gulpfile.js      Файл настроек


УСТАНОВКА НЕОБХОДИМОГО ПО
--------------------------

### Перед использованием gulp pack необходимо установить node.js, а также yarn - быстрый и надежный пакетный менеджер.

Установите node.js перейдя по [этой ссылке](https://nodejs.org/en/download/), для установки пакетного менеджера yarn перейдите по [этой ссылке](https://yarnpkg.com/lang/en/docs/install/).


УСТАНОВКА GULP PACK ЧЕРЕЗ GIT РЕПОЗИТОРИЙ
-------------------------------------------

Чтобы установить gulp pack вы можете скачать архив по ссылке или клонировать репозиторий:

https://github.com/webdesignchannel/optimize_html.git


УСТАНОВКА GULP PACK ЧЕРЕЗ COMPOSER
-------------------------------------------

Установка с помощью композера:

~~~
composer require webdesignchannel/optimize-html:dev-master
composer create-project --prefer-dist webdesignchannel/optimize-html:dev-master
~~~


НАЧАЛО РАБОТЫ
--------------------------------

Для установки зависимостей, откройте терминал из корня рабочей папки и введите команду:

~~~
yarn install
~~~

Для запуска gulp pack введите команду:

~~~
gulp watch
~~~

Для запуска gulp pack для продакшена введите команду:

~~~
gulp production
~~~


ОБНОВЛЕНИЕ ПАКЕТОВ
--------------------------------

Для обновления всех пакетов используйте команду:

~~~
yarn upgrade
~~~

Для обновления определенного пакета используйте команду:

~~~
yarn upgrade [package]@[version]
~~~


НАСТРОЙКА LIVE RELOAD
--------------------------------

Для запуска live reload на локальной машине, в файле gulpfile.js в таске (liveReload) замените конструкцию:

~~~
server: {
	baseDir: "app"
}
~~~

На следующую конструкцию:

~~~
proxy: "ваш локальный домен например (site.local)"
~~~