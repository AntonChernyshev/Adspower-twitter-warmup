## Скрипт для прогрева ваших Твиттеров, которые импортированны в ферму AdsPower
Все понимают, что Твиттеры нужно греть. Я периодически прогреваю свои акки и за 8 месяцев у меня отлетело всего 4 штуки (покупал их по USD 0.12). Этот скрипт поможет сэкономить тебе бешенное количество времени и немного денег. Он работает с профилями Twitter, которые импортированны в [AdsPower](https://share.adspower.net/Btc9YYgpiyJxhmW).

Связь с создателем: https://t.me/CrytoBusher <br>
Если ты больше по Твиттеру: https://twitter.com/CryptoBusher <br>

Залетай сюда, чтоб не пропускать дропы подобных скриптов: https://t.me/CryptoKiddiesClub <br>
И сюда, чтоб общаться с крутыми ребятами: https://t.me/CryptoKiddiesChat <br>

## Преимущества
1. Рандомизация координат, по которым производится клик по кнопке.
2. Рандомизация ввода текста в поле для твита.
3. Рандомизация других задержек.
4. Работа через AdsPower.
5. Отчетность в виде скриншотов.

## Недостатки
1. Однопоточность.
2. Скудный сценарий прогрева.
3. Нет проверки случайно появившихся модалок (смена почты, включение уведомлений). Когда поймаю их - подправлю.

## Логика работы
1. Рандомно выбирается профиль AdsPower.
2. Открывается профиль AdsPower.
3. Осуществляется переход в Твиттер.
4. Рандомная задержка.
5. Осуществляется клик по кнопке "Tweet" с заданным отклонением от стандартных координат. Если клик зафейлился - производится обычный клик.
6. Рандомная задержка.
7. Осуществляется вбив рандомного твита из базы с использованием заданных пользователем задержек.
8. Рандомная задержка.
9. Осуществляется клик по кнопке "Tweet" с заданным отклонением от стандартных координат. Если клик зафейлился - производится обычный клик.
10. Задержка 5 секунд.
11. Скриншот инстанса с последующим сохранением в папку "data/screenshots".
12. Закрытие профиля AdsPower.
13. Задержка, заданная пользователем.
14. Повтор

## Первый запуск
1. Устанавливаем Python 3.10.
2. Качаем репозиторий.
3. Открываем терминал, переходим в папку с файлами и пишем команду "pip install -r requirements.txt".
4. Открываем файл "data/config.py" с помощью любого текстового редактора и подбиваем настройки рандомизации. Все пояснения по настройкам описаны в комментариях в самом файле.
5. Открываем файл "data/profile_ids.py" с помощью любого текстового редактора и забиваем свои профиля как в примере ("название":"ID из AdsPower").
6. Открываем файл "data/tweets.txt" и закидываем базу твитов. Нагенерить можно самому, на фрилансе или в ChatGPT. Чем меньше твитов - тем чаще они будут повторяться, тк они выбираются рандомом.
7. Открываем файл "data/twitter_handles.txt" и забиваем туда свои Twitter Username, так, чтоб они соответствовали аккаунтам, вбитым в файл "data/profile_ids.py". Да, это гемор и не было в этом необходимости сейчас, но это пригодится в дальнейшем, когда я буду добавлять новые фичи.
8. В терминале, находясь в папке проекта, вписываем команду "python3 adspower_twitter_warmup.py" и жмем ENTER.
