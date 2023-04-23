# <img src="https://isoviet.github.io/media/icons/banana/icon.svg" height="64"> Odd Food

[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/isoviet/odd-food.svg)](http://isitmaintained.com/project/isoviet/odd-food "Average time to resolve an issue") [![Percentage of issues still open](http://isitmaintained.com/badge/open/isoviet/odd-food.svg)](http://isitmaintained.com/project/isoviet/odd-food "Percentage of issues still open")

--------------

* [О проекте](#о-проекте)
* [Установка](#установка)
* [Технология](#технология)

## О проекте
Odd Food — утилита, позволяющая внедрить произвольную полезную нагрузку в изображение. На данный момент поддерживаются только изображения формата PNG (Portable Network Graphics).

Автор Odd Food не несёт ответственности за использование утилиты в противоправных целях третьими лицами. Законотворцам рекомендуется ознакомиться с [этой информацией](https://ru.wikipedia.org/wiki/Умысел).

## Установка
Для установки Odd Food необходимо скачать и запустить последнюю версию установщика со [страницы загрузки](https://github.com/isoviet/odd-food/releases). Утилита запускается через командную строку командой "odd-food" со следующими аргументами:

<table><thead><tr><th>Argument</th><th>Description</th></tr></thead><tbody><tr><td>--act</td><td>Action (pack/unpack)</td></tr><tr><td>--pld</td><td>Payload file path (for packing)</td></tr><tr><td>--in</td><td>Input file path</td></tr><tr><td>--out</td><td>Output file path</td></tr></tbody></table>

## Технология
Odd Food Payload Format
<table><thead><tr><th rowspan=2>Offset</th><th align="center" colspan=22>Trits</th></tr><tr><th>0</th><th>1</th><th>2</th><th>3</th><th>4</th><th>5</th><th>6</th><th>7</th><th>8</th><th>9</th><th>10</th><th>11</th><th>12</th><th>13</th><th>14</th><th>15</th><th>16</th><th>17</th><th>18</th><th>19</th><th>20</th><th>21</th></tr></thead><tbody><tr><td>0x0</td><td colspan=22>Magic (14544909)</td></tr><tr><td>0x15</td><td colspan=22>Length</td></tr><tr><td>0x2A</td><td colspan=22>Data</td></tr></tbody></table>

Odd Food Pixel Storage
<table><thead><tr><th>Channel</th><th>0</th><th>1</th><th>2</th><th>3</th><th>4</th><th>5</th><th>6</th><th>7</th></tr></thead><tbody><tr><td>Red</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>✔️ (1;3)</td><td>✔️ (1;2)</td><td>✔️ (1;1)</td></tr><tr><td>Green</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr><tr></tr><tr><td>Blue</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>✔️ (2;3)</td><td>✔️ (2;2)</td><td>✔️ (2;1)</td></tr><tr><td>Alpha</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr></tbody></table>

Odd Food Image Sizes
<table><thead><tr><th>Size</th><th>Max payload length</th></tr></thead><tbody><tr><td>128x128</td><td>6.3K</td></tr><tr><td>256x256</td><td>25.3K</td></tr><tr><td>512x512</td><td>101.4K</td></tr><tr><td>1024x768</td><td>304.3K</td></tr><tr></tr><tr><td>1024x1024</td><td>405.7K</td></tr><tr><td>2560x1440</td><td>1.39M</td></tr></tbody></table>
