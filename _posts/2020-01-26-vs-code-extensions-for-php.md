---
title: Полезные расширения VS Code для работы с PHP
layout: post
thumb: /images/vs-code-extensions-for-php/thumb.png
thumb_small: /images/vs-code-extensions-for-php/thumb_small.png
---

В этой статье хочу рассмотреть расширения для Visual Studio Code, которыми пользуюсь при разработке на PHP.

Набор основан на личном опыте. Возможно, я упустил какие-то другие хорошие расширения. Буду рад, если вы мне сообщите о них.

Здесь будут приведены только общие расширения для PHP в целом. Никаких специфичных для фреймворков.

Давайте перейдем непосредственно к списку.

## [PHP Intelephense](https://marketplace.visualstudio.com/items?itemName=bmewburn.vscode-intelephense-client){:target="_blank"}

![PHP Intelephense autocomplete](/images/vs-code-extensions-for-php/vs-code-php-autocomplete.gif)

По умолчанию, VS Code предлагает очень общие подсказки, которые не всегда помогают при разработке на PHP. Улучшить эту ситуацию может расширение PHP Intelephense. С ним писать код станет значительно комфортней.

Единственная проблема, которая меня раздражала - это повторяющиеся подсказки.

![Проблемы с подсказками](/images/vs-code-extensions-for-php/suggestions-problem.png)

Возможно эта проблема задевала только меня, но тем не менее, я избавился от нее отключением базовых (не всех) подсказок PHP. В настройках это `php.suggest.basic`. Подсказки по-прежнему работают, но не повторяются.

Также есть альтернатива данному расширению - [PHP IntelliSense](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-intellisense){:target="_blank"}. При том, что оно более популярно (по крайней мере по скачиваниям), я считаю, что оно уступает по возможностям и по удобству работы в целом. Поэтому вместо него рекомендую **PHP Intelephense**.

## [PHP DocBlocker](https://marketplace.visualstudio.com/items?itemName=neilbrayfield.php-docblocker){:target="_blank"}

Расширение, которое помогает писать блоки с комментариями к классам, функциям и т.д. Просто начинаете печатать `/**` и жмете Enter. Оно само определяет входные данные и возвращаемое значение функции (если они есть). Также предоставляет шаблоны, например, если начнете внутри блока с комментариями писать `@`.

## [phpfmt - PHP formatter](https://marketplace.visualstudio.com/items?itemName=kokororin.vscode-phpfmt){:target="_blank"}

Очень удобно одной командой отформатировать php-файл. Не сказал бы, что часто может понадобиться, но такие случаи бывают.

## [PHP Debug](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-debug){:target="_blank"}

![PHP Debug](/images/vs-code-extensions-for-php/php-debug.gif)

Мощное расширение для дебаггинга, которое добавляет поддержку **XDebug**. Придется потратить время на то, чтобы настроить данное расширение, но оно того стоит. Также есть возможность делать дебаггинг на удаленном сервере (честно еще не пользовался).

## Заключение

Безусловно, расширений для PHP еще очень много, но я привел только тот минимум, которым я пользуюсь сейчас. Я пробовал и другие, но по разным причинам от них отказался.
Да и сильно перегружать VS Code расширениями не хочется, ведь кроме этих, у меня есть расширения для фреймворков, HTML, CSS, JS, Git и т.д.

На этом все, пишите какие расширения для PHP используете вы.