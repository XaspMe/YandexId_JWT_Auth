# OAUTH через YandexId
## Пример использования аутентификации в дотнет приложении с помощью [YandexId](https://oauth.yandex.ru/ ).

- Создать [тут](https://oauth.yandex.ru/client/new/id) новое приложение
- Скопировать clientId и clientSecret своего приложения на строки 23 и 24 этого приложения (Program.cs)
- Пройти по ссылке из эндпоинта /authorize авторизоваться яндексом и забрать ключ (он работает 10 минут, после чего обновится) - вот [документация на эндпоинт](https://yandex.ru/dev/id/doc/ru/codes/code-url)
- Используя ключ из /authorize забрать AccessToken из /get_token документация тоже [тут](https://yandex.ru/dev/id/doc/ru/codes/code-url)
- Используя AccessToken из /get_token можно получить [клеймы пользователя](https://yandex.ru/dev/id/doc/ru/user-information) по эндпоинту /whoami и по ним строить авторизацию в вашем приложении !!! таже тут можно вместо json получить JWT
- ✨Magic ✨
- [Обновить AccessToken можно используя refresh_token](https://yandex.ru/dev/id/doc/ru/tokens/refresh-client)
