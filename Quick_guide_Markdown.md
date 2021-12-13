# Краткое руководство по Markdown

Абзацы создаются при помощи пустой строки. Если вокруг текста сверху и снизу есть пустые строки, то текст превращается в абзац.

Чтобы сделать перенос строки вместо абзаца,  
нужно поставить два пробела в конце предыдущей строки.

Заголовки отмечаются диезом `#` в начале строки, от одного до шести. Например:

# Заголовок 1
## Заголовок 2
### Заголовк 3
#### Заголовк 4
##### Заголовк 5
###### Заголовок 6

В декоративных целях заголовки можно «закрывать» с обратной стороны.

***

## Списки

Для разметки неупорядоченных списков можно использовать или `*`, или `-`, или `+`. Вложенные пункты создаются четырьмя пробелами перед маркером пункта:

* элемент 1
    * вложенный элемент 1
    * вложенный элемент 2
- элемент 2
+ элемент 3

Упорядоченный список:

1. элемент 1
2. элемент 2
    1. вложенный
    2. вложенный
3. элемент 3

На самом деле не важно как в коде пронумерованы пункты, главное, чтобы перед элементом списка стояла цифра (любая) с точкой. Можно сделать и так:

0. элемент 1
0. элемент 2
0. элемент 3
0. элемент 4

Список абзацами:

* раз абзац
* два абзац
* три абзац

***

## Цитаты

Цитаты оформляются как в емейлах, с помощью символа `>`.

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

Или более ленивым способом, когда знак `>` ставится перед каждым элементом цитаты, будь то абзац, заголовок или пустая строка:

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.

В цитаты можно помещать всё что угодно, в том числе вложенные цитаты:

> ## This is a header.
>
> 1.   This is the first list item.
> 2.   This is the second list item.
>
> > Вложенная цитата.
>
> Here's some example code:
>
>     return shell_exec("echo $input | $markdown_script");

***

## Горизонтальная черта

`hr` создается тремя звездочками или тремя дефисами.

***

## Ссылки

Это встроенная [ссылка с title элементом](http://example.com/link "Я ссылка"). Это — [без title](http://example.com/link).

А вот [пример][1] [нескольких][2] [ссылок][id] с разметкой как у сносок. Прокатит и [короткая запись][] без указания id.

[1]: http://example.com/ "Optional Title Here"
[2]: http://example.com/some
[id]: http://example.com/links (Optional Title Here)
[короткая запись]: http://example.com/short

Вынос длинных урлов из предложения способствует сохранению читабельности исходника. Сноски можно располагать в любом месте документа

***

## Выделение слова

Выделять слова можно при помощи `*` и `_`. Одним символ для наклонного текста, два символа для жирного текста, три — для наклонного и жирного одновременно.

Например, это _italic_ и это тоже *italic*. А вот так уже __strong__, и так тоже **strong**. А так ***жирный и наклонный*** одновременно.

***

## Зачеркивание

В GFM добавлено зачеркивание текста: две тильды `~` до и после текста.

~~Зачеркнуто~~

***

## Картинки

Базовый синтаксис Markdown для внедрения изображения:

`![<alt text>](<folderPath>)`

Example:

![alt text for image](енот4.jpg)

Где `alt text` — краткое описание изображения, а `folder path` — относительный путь к нему. Заменяющий текст необходим для средств чтения с экрана для слабовидящих. Он также удобен при возникновении ошибок на сайте, из-за которых не удается воспроизвести изображение.

Запомнить просто: синтаксис как у ссылок, только перед открывающей квадратной скобкой ставится восклицательный знак.

Картинки «сноски»:

![Картинка1][image1]
![Картинка2][image2]
![Картинка3][image3]

[image1]: енот1.jpg
[image2]: енот2.jpg
[image3]: енот3.jpg

Картинки-ссылки:

[![Вот вам еще енот](https://pristor.ru/wp-content/uploads/2019/09/Еноты-прикольные-картинки-и-фото-11.jpg)](https://pristor.ru/enoty-prikolnye-kartinki-i-foto/)

***

## Таблицы

В чистом **Markdown** нет синтаксиса для таблиц, а в **GitHub-Flavored Markdown** есть.

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

Для красоты можно и по бокам линии нарисовать:

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

Можно управлять выравниванием столбцов при помощи двоеточия.

| Left-Aligned  | Center Aligned  | Right Aligned |
|:------------- |:---------------:| -------------:|
| col 3 is      | some wordy text |     **$1600** |
| col 2 is      | centered        |         *$12* |
| zebra stripes | are neat        |        ~~$1~~ |

Внутри таблиц можно использовать ссылки, наклонный, жирный или зачеркнутый текст.

~~зачеркнутый текст~~

__это же полужирный шрифт__

_а это курсив_

|X|O|X|

|O|X|O|

|X|O|X|

##Создание ветки
Используется команда `git branch`. Например `git branch name`
