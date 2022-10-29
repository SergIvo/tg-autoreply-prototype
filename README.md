# Автоответчик ТГ #

Прототип приложения-автоответчика для Телеграма.

Сделано по туториалам отсюда: [https://github.com/alexander-akhmetov/python-telegram](https://github.com/alexander-akhmetov/python-telegram)

Для запуска необходимо установить зависимости из `requirements.txt`, а также переменные окружения:

```
TG_API_ID=Идентификатор приложения
TG_API_HASH=Хэш идентификатора приложения
PHONE_NUMBER=Номер телефона или тэг Телеграм-бота
DB_ENCRYPTION_KEY=Случайный ключ
```
Чтобы получить идентификатор приложения и его хэш, нужно пройти по адресу [https://my.telegram.org](https://my.telegram.org), залогиниться и создать приложение. В Device указать desktop (по крайней мере на данный момент).

Номер телефона должен быть привязан к тому аккаунту, от имени которого будет писать автоответчик.

Случайный ключ по-видимому можно взять любой.

Автоответчик срабатывает в нерабочие часы. Расписание на данный момент забито прямо в код.

При первом запуске приложения потребуется ввести код подтверждения логина. Запрос на ввод должен появиться в консоли. При последующих запусках приложение не требует повторного ввода кода, но где и как долго API хранит данные сессии, пока не понятно.

В документации упомянута [возможность](https://python-telegram.readthedocs.io/en/0.16.0/non_blocking_login.html) другого варианта логина, но она пока не проверялась.