# <p align="center">Ubilling Bot Feedback

<p align="center">Telegram/Viber Feedback Bot

  * [Возможности](#Возможности)
  * [Как этим пользоваться](#Как-этим-пользоваться)
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

❌ - Показывать тикеты пользователя

✅ - Оповещать пользователей за 3 дня до конца предоставления услуг (Время отправки рассылки настраивать можно через крон, например)</br>

## Как этим пользоваться

В этом репозитории есть <a href="https://github.com/Fenicu/Ubilling-Bot-Feedback/blob/master/texts.ini">ini</a> файл настроек бота, там настраиваются все тексты и кнопки

Так же возможно отключить модуль службы поддержки и оставить только личный кабинет абонента</br>
В ini файле описано что, где, для чего

Небольшой пример заполнения ini файла, например, отображения личного кабинета абона для <b>ТЕЛЕГРАМА</b></br>
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

## Где получить это чудо

Получить это чудо можно у <a href="https://t.me/Fenicu">разработчика в телеграме</a></br>
Я обычное физ лицо, переводить <s>600$</s> 450$ вам придётся в Россию, на карту сбербанка</br>
Бот написан на `python 3.7`</br>
`aiohttp, aiogram, viberio`

## Что требуется для быстрого деплоя

Подготовьте VPS</br>
`Ubuntu 20.04.1 LTS`</br>
`1GB ОЗУ`</br>
`15GB HDD`</br>
`Домен`

Бота деплоить буду я, от вас только железо и заполненный <a href="https://github.com/Fenicu/Ubilling-Bot-Feedback/blob/master/texts.ini">ini файл</a>

## Демка

<a href="https://t.me/joinchat/D_IHsVQVfjyZtJj-WYu01A">Демо чат для тестирование ответов</a>

<a href="https://t.me/UbillingFeedbackDemoBot">Телеграм демо</a>

<a href="https://redirect.fenicu.men/viberdemo">Вайбер демо</a></br>
`viber://pa?chatURI=ubillingfeedbackdemo`


<a href="https://redirect.fenicu.men/NGGYU">do not click</a>