# Центрование попапа

## Решение задачи

Центруем попап при помощи браузера и свойств "display: table;", "display: table-cell;",
"vertical-align: middle;" и "margin: 0 auto;".

### Достоинства

* Все расчеты проводятся браузером
* Минимум JS и можно обойтись нативным

### Недостатки

* Некоторая избыточность тегов
* Необходимо уделять большое внимание разрешению экранов (media queries), чтобы не приходить
  к положению, когда например нельзя закрыть попап, потому что ссылка на закрытие вне viewport-а.
* Ширина попапа фиксированная

### Итого

Способ работает на всех современных браузерах и, если уделять должное внимание адаптивности,
то и на всех экранах.

Другие способы CSS-центрования не рассматриваю, т.к. они накладывают ограничение либо
на родительский блок, либо на центруемый. Соответсвенно необходимы JS-извращения на каждый resize,
включая и первый.

<hr />

# Альтернативные способы:

## №2 Все расчеты на JS

На стороне CSS остается только оформление и "position: absolute;"

### Достоинства

* Полный контроль над положением и другими свойствами попапа
* При правильном подходе работает везде, где есть JS
* Никаких лишних тегов - генерируем все на лету

### Недостатки

* Нагрузка на JS-движок браузера
* Сложности в разработке (jQuery конечно облегчает)

## №3 Комбинированый способ

Выравнивание происходит при помощи CSS, расчет критичных параметров через JS.

Комбинирует достоинства и недостатки предыдущих двух методов.
Позволяет пользоваться другими способами вертикального CSS-выравнивания.

## №4 Воспользоваться существующей библиотекой

Например в jQuery UI есть удобный виджет Dialog с большим количеством настроек и возможностей.

### Достоинства

* Все сделали уже за вас

### Недостатки

* Размер библиотек
* Избыточный функционал
* Сложная кастомизация
* Возможно недостаточное покрытие устройств
