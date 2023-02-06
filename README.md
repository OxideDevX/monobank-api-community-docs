# Monobank API community docs

<img alt="logo" src="https://user-images.githubusercontent.com/59166229/211002581-faa622e4-d47f-4c93-9d9d-afce50484339.png" width="200" height="200" />

Більшість інформації у поточному репозиторії буде відноситись саме до Monobank open API.

Щодо інших API див. інформацію [нижче](#інші-api-створені-командою-mono).

> Інформація структурована силами community користувачів Monobank API на основі
> практичного досвіду використання або зворотнього зв'язку представників Monobank у 
> Telegram чаті community (посилання на чат доступне на сторінці документації до API)

## API

Monobank Open API - API що доступне публічно (без аутентифікації), або клієнтам банку за токеном аутентифікації,
або провайдерам послуг.

Link на документацію щодо Monobank Open API:
- загальний https://api.monobank.ua/docs/
- корпоративний API для провайдерів послуг https://api.monobank.ua/docs/corporate.html

Розробкою цієї частини API займається лише один розробник Monobank за власною ініціативою та займається його розвитком
у вільний час. З чого випливає, що можливості його розширення або підтримки щодо питань досить обмежені.

За багатьма причинами (в тому числі - безпековими) Open API надає можливість використання лише "Read-only" операції.
Можливостей формування тих чи інших транзакцій або змінювання даних клієнту немає.

Тільки розробник може надати _абсолютно точну та вичерпну_ інформацію по даному API.

### Корпоративний API для провайдерів послуг

"Production" доступ до API надається ЛИШЕ після підтвердження заявки відправленої через API: 
https://api.monobank.ua/docs/corporate.html#tag/Avtorizaciya-ta-nalashtuvannya-kompaniyi/paths/~1personal~1auth~1registration/post

Алгоритм підпису запитів до API ("X-Sign" HTTP header): https://gist.github.com/Sominemo/64845669d6326f2f73d356f025656bdb#signing-the-request

## Telegram API community

У Telegram створено чат для спільноти користувачів Monobank Open API для наступного:
- надання зворотного зв'язку щодо користування API;
- взаємодопомога користувачів щодо питань використання API;

Для збереження балансу корисної інформації у чаті та економії часу інших учасників чату, вважається хорошим тоном:
- не використовувати чат як фріланс біржу;
- не використовувати чат як "кружок програмістів";
- обговорювати теми близькі саме до питань користування Monobank Open API;
- поважати час інших та ознайомлюватись з інформацією наданою тут, у закріплених повідомленнях чату, документації.

> Посилання на чат доступне на сторінці документації до API.

## Troubleshooting

### 1. Помилка при зверненні до API - 403 status code з HTML у тілі відповіді

Якщо при роботі з API Ви отримуєте помилку 403 - скоріше за все вас заблокував AWS 
(що "захищає" API від атак зловмисників).

Нажаль, ні розробники (представники банку), ні community не можуть допомогти з розблокуванням.

Тіло відповіді може виглядати наступним чином:
```
 <html>
    <head>
      <title>403 Forbidden</title>
    </head>
    
    <body>
      <center>
        <h1>403 Forbidden</h1>
      </center>
    </body>
</html>
```

## Інші API створені командою mono 

Monobank має не тільки open API, але й інші:
1. Інтернет-еквайринг
2. Покупка частинами
3. Expirenza by mono (shaketopay)

Щодо даних сервісів Вам можуть надати консультацію співробітники Monobank, до яких Ви можете звернутись
за каналами комунікації що надані на лендінг сторінках сервісів.

### 1. Інтернет-еквайринг (acquiring)

Посилання на лендінг сторінку сервісу: https://monobank.ua/e-comm

Посилання на документацію: https://api.monobank.ua/docs/acquiring.html

Офіційний модуль WordPress від Monobank для підключення інтернет-еквайрингу: https://uk.wordpress.org/plugins/monopay/

### 2. Покупка частинами

Посилання на лендінг сторінку сервісу: https://chast.monobank.ua/vendors

Посилання на документацію: https://u2-demo-ext.mono.st4g3.com/docs/index.html

### 3. Expirenza by mono (shaketopay)

Посилання на лендінг сторінку сервісу: https://shaketopay.com.ua/

Посилання на документацію: https://api.shaketopay.com.ua/
