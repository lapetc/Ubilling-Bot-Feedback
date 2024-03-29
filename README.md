# <p align="center">Ubilling Bot Feedback

<p align="center">Telegram/Viber Feedback Bot

  * [Возможности](#Возможности)
  * [Как этим пользоваться](#Как-этим-пользоваться)
  * [Мультиязычность](#Мультиязычность)
  * [Где получить это чудо](#Где-получить-это-чудо)
  * [Что требуется для быстрого деплоя](#Что-требуется-для-быстрого-деплоя)
  * [Демка](#Демка)

## Возможности
Проект из себя представляет бота для Телеграма и Вайбера в одном флаконе

Саппорт сидит в телеге и отвечает на сообщения всех пользователей</br>
Да, вам больше не придётся заходить в вайбер, за это можете докинуть на чай денежку

В себе имеет личный кабинет абонента, работает на <a href="http://wiki.ubilling.net.ua/doku.php?id=xmlagent">Ubilling API (XMLAgent)</a>

Бот может:

✅ - Показывать ссылки для оплаты услуг</br>
Посмотреть какие ссылки можно показать абону для <a href="http://wiki.ubilling.net.ua/doku.php?id=xmlagent#платежные_системы">оплаты услуг</a>

✅ - Показывать тариф, баланс, кредит, когда он истекает</br>
Посмотреть какие данные можно показать абону по <a href="http://wiki.ubilling.net.ua/doku.php?id=xmlagent#общие_данные_пользователя_но_с_авторизацией">кабинету тут</a>

✅ - Показывать историю платежей</br>
Посмотреть какие данные можно показать абону по <a href="http://wiki.ubilling.net.ua/doku.php?id=xmlagent#информация_о_предыдущих_платежах_пользователя">истории платежей</a>

✅ - Показывать активные объявления кабинета пользователя</br>
Посмотреть какие данные можно показать абону по <a href="http://wiki.ubilling.net.ua/doku.php?id=xmlagent#активные_объявления_кабинета_пользователя">объявлениям кабинета</a>

✅ - Оповещать пользователей за 3 дня до конца предоставления услуг (Время отправки рассылки настраивать можно через крон, например)</br>

✅ - Абоненты могут брать <a href="http://wiki.ubilling.net.ua/doku.php?id=xmlagent#кредитование">кредиты</a>

✅ - [Мультиязычность](#Мультиязычность)

## Как этим пользоваться

В этом репозитории есть <a href="https://github.com/Fenicu/Ubilling-Bot-Feedback/blob/main/config.ini">ini</a> файл настроек бота, там настраиваются все тексты и кнопки

Так же возможно отключить модуль службы поддержки и оставить только личный кабинет абонента</br>
В ini файле описано что, где, для чего

Небольшой пример заполнения конфиг файла, например, отображения личного кабинета абона для <b>ТЕЛЕГРАМА</b></br>
<i>Вайбер не поддерживат HTML разметку</i>

```ini
show_cabinet=Привет, <b>{realname}</b>!
    Логин: <b>{bil_login}</b>
    IP адрес: <b>{ip}</b>
    Номер телефона: <b>{mobile}</b>
    Статус аккаунта: <b>{accountstate}</b>
    Тариф: <b>{tariff}</b>
    Баланас: <b>{cash} {currency}</b>
    Кредит: <b>{credit}</b>
    Кредит истекает: <b>{creditexpire}</b>
    Платёжный айди: <b>{payid}</b>
```

## Мультиязычность
Добавлять можно любую локализацию, она состоит из ini файлов, достаточно положить ini файлик со своей локализацией в папку /locale
```ini
[GLOBAL]
; Текст на кнопке с выбором языка
locale_name=🇺🇦Український
; Код локализации - значение в бд, они не должны повторяться
locale_code=ua
```
```ini
[GLOBAL]
; Текст на кнопке с выбором языка
locale_name=🇧🇾Беларускі
; Код локализации - значение в бд, они не должны повторяться
locale_code=by
```
```ini
[GLOBAL]
; Текст на кнопке с выбором языка
locale_name=🇷🇺Русский
; Код локализации - значение в бд, они не должны повторяться
locale_code=ru
```
```ini
[GLOBAL]
; Текст на кнопке с выбором языка
locale_name=🦄Юбиллинговый
; Код локализации - значение в бд, они не должны повторяться
locale_code=ubilling
```
```ini
[GLOBAL]
; Текст на кнопке с выбором языка
locale_name=🙈Любой другой🙈
; Код локализации - значение в бд, они не должны повторяться
locale_code=any
```

Не забудьте указать язык по умолчанию в <a href="https://github.com/Fenicu/Ubilling-Bot-Feedback/blob/main/config.ini">config.ini</a>
```ini
[GLOBAL]
; locale_code локализация по умолчанию
locale_default=ua
```
ВНИМАНИЕ, НЕ РЕКОМЕНДУЕТСЯ ИСПОЛЬЗОВАТЬ ЛОКАЛИЗАЦИЮ ИЗ ПРИМЕРОВ ПО ПОНЯТНОЙ ПРИЧИНЕ, ПРОСТО УДАЛИТЕ ПРИМЕРЫ И СДЕЛАЙТЕ СВОЮ ЛОКАЛИЗАЦИЮ

## Где получить это чудо

Получить это чудо можно у <a href="https://t.me/Fenicu">разработчика в телеграме</a></br>
Ценник 450$ за полный комплект с деплоем на ваш сервер</br>
Если нужен только телеграм или вайбер, делите цену на два  (225$)</br>
Доработка платформ — обсуждаемое дело как и любой другой функционал</br>
Если вам нужно что-то особенное, пожалуйста, пришлите ТЗ (техническое задание) в виде блок-схем</br>

Так же можно взять это чудо с подпиской 15$/месяц</br>
В таком случаи от вас только информация куда, что, чего. Остальное беру на себя

Бот написан на `python 3.8.5`</br>
`aiohttp, aiogram, viberio`

## Что требуется для быстрого деплоя

Подготовьте VPS</br>
`Ubuntu 20.04.1 LTS`</br>
`1GB ОЗУ`</br>
`15GB HDD`</br>
Выделять айпишник не обязательно, достаточно `443` и `80` порты (требуется для сертификата, вайбер ещё тот козёл и не кушает селфсингед)

Бота деплоить буду я, от вас только железо и заполненный <a href="https://github.com/Fenicu/Ubilling-Bot-Feedback/blob/main/config.ini">config.ini</a> (он требуется сразу, чтобы я мог проверить работоспособность ботов)</br>

Конфиг файл можно изменять в любой момент как и добавлять локализации, достаточно просто перезапустить бота

## Демка

<a href="https://t.me/joinchat/D_IHsVQVfjyZtJj-WYu01A">Демо чат для тестирование ответов</a>

<a href="https://t.me/UbillingFeedbackDemoBot">Телеграм демо</a>

<a href="https://redirect.fenicu.men/viberdemo">Вайбер демо</a></br>
`viber://pa?chatURI=ubillingfeedbackdemo`


<a href="https://redirect.fenicu.men/NGGYU">do not click</a>
