#Simple Callback Module#
Простой модуль обратного звонка или для обратной связи. Совместим с Joomla 3.0 и выше.

**Основные преимущества:**

 1. Бесплатный
 2. Безопасный: поддержка токенов ([CSRF](https://docs.joomla.org/How_to_add_CSRF_anti-spoofing_to_forms))  и капчи
 3. Возможность вставки нескольких модулей на одну страницу
 4. Содержит все необходимые настройки

Модуль поддерживает несколько видов отображения на странице:

 - *Как обычный модуль* —  форма вставляется в указанную позицию
 - *Как оверлей* — код формы вставлен в позицию, но сама форма скрыта. Вызвать
   форму можно с любой кнопки на странице с аттрибутом
   **data-simplecallback**, например:

```
<a href="#" data-simplecallback>
    Обратная связь
</a>
```

Еще вызвать модуль можно через JS:

```javascript
/* показать оверлей с модулем по id */
    simplecallback.show(id); 
/* скрыть оверлей с модулем */
    simplecallback.hide(); 
```

В коде сверху вызовется самый первый модуль с оверлеем. Если на странице размещается сразу несколько модулей, то вызвать нужный можно указав ID модуля в аттрибуте data-simplecallback, например:

```
<a href="#" data-simplecallback="93">
    Обратный звонок
</a>
```

Модуль создан без особого прицела на визуальный дизайн, т.к. дизайн каждого сайта индивидуален, поэтому вам предоставляется полная свобода для оформления и верстки. Тем не менее, чуть позже будут добавлены несколько тем, например bootstrap-совместимая.

**Что будет дальше:**

 - Поддержка SMS шлюзов, например sms.ru для уведомления администратора
   сайта
 - Компонент com_simplecontact в котором будут сохраняться все
   отправленные данные
