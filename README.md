# Grid-system
## 1. Стили страницы:
  1.1 Основные в _page.less;  

  1.2 Шрифты в _font.less;

  1.3 Все они собираются в libs.less, а затем в libs.css:

```php
  @import "_font.less";

  @import "_page.less";
```

## 2. Стили сетки:
  1.1 Переменные находятся в _var.less;

  1.2 Основная сетка в _grid.less, в нее также подлкючаются шрифты и переменные, ее и подключаем в главный файл style.less:

```php
  @import "_grid.less";
```

## 3. Разметка:
  3.1 Работа с контейнером:
```php
  blocks{
    .container();//фиксированная ширина
    .container-fluid();//ширина на всю страницу
  }
```
  3.2 Работа со строкой:
```php
  block{
    .row();//строка
    .lg,md,sm,xs({атрибуты css});//добавляем строке атрибуты css по размерам экрана 
    .justify, .justify-(lg,md,sm,xs)(значение justify-content);//добавляем атрибут align-items стандартно или адаптивно (flex-start по умолчанию)
    .align, .align-(lg,md,sm,xs)(значение align-items);//добавляем атрибут align-items (stretch по умолчанию)

  }
```
  3.3 Работа с ячейкой:
```php
  block-item{
    .col(1-12);//назначаем блок ячейкой и устанавливаем ей ширину на всех размерах (1 по умолчанию) 
    .size(1-12), .size-(lg,md,sm,xs)(1-12);//устанавливаем размер ячейки стандартно или адаптивно
    .lg,md,sm,xs({атрибуты css});
    .justify, .justify-(lg,md,sm,xs)(значение justify-content);
    .align, .align-(lg,md,sm,xs)(значение align-items);
  }
```
  3.4 Работа с таблицей:
```php
  block-item{
    table{
      .table();//задаем стили таблицы
      .thead-dark(), .thead-light();//Названия столбцов темная или светлая (по умолчанию светлая)      
      .table-border();//Добавляем строкам и ячейкам границы по всем фронтам
      .table-border-bottom();//Добавляем строкам только 1 границу снизу
    }
  }
```
3.5 Работа с картинками:
```php
  block-item{
    img{
      .img-fluid();//Картинку на всю ширину
      .rounded();//Округление углов
      .img-thumbnail();//Добавление рамки к картинке
    }
  }
```



