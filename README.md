# <img src="https://isoviet.github.io/media/icons/banana/icon.svg" height="64"> Odd Food

[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/isoviet/odd-food.svg)](http://isitmaintained.com/project/isoviet/odd-food "Average time to resolve an issue") [![Percentage of issues still open](http://isitmaintained.com/badge/open/isoviet/odd-food.svg)](http://isitmaintained.com/project/isoviet/odd-food "Percentage of issues still open")

--------------

* [О проекте](#о-проекте)
* [Установка](#установка)
* [Технология](#технология)

## О проекте
Odd Food — утилита, позволяющая внедрить произвольную полезную нагрузку в изображение. На данный момент поддерживаются только изображения формата PNG (Portable Network Graphics).

Автор Odd Food не несёт ответственности за использование утилиты в противоправных целях третьими лицами. Законотворцам рекомендуем ознакомиться с [этой информацией](https://ru.wikipedia.org/wiki/Умысел).

## Установка
Для установки Odd Food необходимо скачать и распаковать [этот репозиторий](https://github.com/isoviet/oddfood/archive/refs/heads/master.zip), после чего запустить требуемый скрипт (pack.py/unpack.py), указав необходимые аргументы.

Для работы плагина необходим установленный [Python 3](https://www.python.org/downloads/).

## Технология
Odd Food Payload Format
<table><thead><tr><th>Offset</th><th>0</th><th>1</th><th>2</th><th>3</th><th>4</th><th>5</th><th>6</th><th>7</th></tr></thead><tbody><tr><td>0x0</td><td colspan=8>Magic (14544909)</td></tr><tr><td>0x8</td><td colspan=8>Length</td></tr><tr><td>0x16</td><td colspan=8>Data</td></tr></tbody></table>

Odd Food Data Storage
<table><thead><tr><th>Channel</th><th>0</th><th>1</th><th>2</th><th>3</th><th>4</th><th>5</th><th>6</th><th>7</th></tr></thead><tbody><tr><td>Red</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>✔️</td><td>✔️</td><td>✔️</td></tr><tr><td>Green</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr><tr></tr><tr><td>Blue</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>✔️</td><td>✔️</td><td>✔️</td></tr><tr><td>Alpha</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr></tbody></table>

Odd Food Image Sizes
<table><thead><tr><th>Size</th><th>Max payload length</th></tr></thead><tbody><tr><td>128x128</td><td>4K</td></tr><tr><td>256x256</td><td>16K</td></tr><tr><td>512x512</td><td>64K</td></tr><tr><td>1024x768</td><td>192K</td></tr><tr></tr><tr><td>1024x1024</td><td>256K</td></tr><tr><td>2560x1440</td><td>900K</td></tr></tbody></table>
