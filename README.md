# jutsu-achievements

Скрипт для автоматической накрутки достижений на профиль jut.su. В минуту ставит примерно 100-150 достижений.

## Установка

Используйте [pip](https://pip.pypa.io/en/stable/), чтобы установить библиотеки.

```bash
pip install requests
pip install lxml
pip install beautifulsoup4
```

## Использование

Скопировать куки с уже авторизованным аккаунтом в файл cookies.txt, после чего зайти на сайт jut.su выбрать любое аниме. Нажать Ctrl + Shift + I -> Network (Сеть), включаем плеер с аниме и ждем появления нового запроса, где имеется ключ the_login_hash
```python
login_hash = "Ключ ваш the_login_hash"
headers = {
    "user-agent": "Тут ваш user agent",
    "cookie": open("cookies.txt", "r").read(),
}
```

После настройки запускаем скрипт и вводим в консоли имя категории (сезона) из адресной строки, например:
```
https://jut.su/mahoutsukai-no-yome/episode-6.html  Из такой ссылки
mahoutsukai-no-yome Получится такое имя категории
```
И запускаем скрипт.


## License
[MIT](https://choosealicense.com/licenses/mit/)
