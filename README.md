# Course_Project_MYSQL_AI
## Kinofin
### Курсовая работа по базам данных факультет Artificial Intelligence

Требования к курсовому проекту
1 Составить общее текстовое описание БД и решаемых ею задач;
2 минимальное количество таблиц - 10;
3 скрипты создания структуры БД (с первичными ключами, индексами, внешними ключами);
4 создать ERDiagram для БД;
5 скрипты характерных выборок (включающие группировки, JOIN'ы, вложенные таблицы);
6 представления (минимум 2);
7 хранимые процедуры / триггеры;
* **Примеры: описать модель хранения данных популярного веб-сайта: кинопоиск, booking.com, wikipedia, интернет-магазин, geekbrains, госуслуги...

Думайте об этом задании, как о том, чем Вы похвастаетесь на своем следующем собеседовании.

Описание проекта
Kinofin - упрощенная модель хранения данных сервиса IMDb с добавлением элементов социальной сети и акцентом на составление списков.

Всё начинается с самых простых, редко изменяющихся данных: список стран, кинокомпаний, жанров, всевозможных профессий/позиций в производственном процессе и список типов экранных сущностей (так как это могут не только фильмы, но и, например, сериалы, в базе они называются абстрактно titles).

TITLES
Ключевые характеристики:
Название
Оригинальное название (необязательно)
Дополнительные характеристики:
Тип (фильм, сериал, анимация, короткометражка и тд)
Постер
Теглайн
Синопсис
Дата выхода
Возрастное ограничение
Состав съемочной группы
Компания-производитель (может быть несколько)
Страна (может быть несколько)
Жанр (может быть несколько)
USERS
Главная движущая сила сервиса – это, естественно, пользователи Их регистрационные данные (таблица users):

Username
Email
Номер телефона
Пароль
Дополнительная информация, которую пользователь может предоставить, заполнив свой профиль:

Аватар
Имя
Фамилия
Дата рождения
Страна
О себе
Приватность аккаунта
Самое интересное кроется в возможностях пользователя, которые в MovieLista достаточно обширны.

ИТАК, ПОЛЬЗОВАТЕЛИ МОГУТ:
Действия с другими пользователями:

Подписываться друг на друга
Переписываться друг с другом
Действия со списками:

Добавлять фильмы в список «Буду смотреть»
Отправлять фильмы в список «Просмотрено»
Создавать свои собственные списки фильмов (например, сохраняя свои поисковые запросы: «хочу все китайские дорамы про вампиров, вышедшие после 2000» или совсем просто – «мои любимые сериалы отобранные мной вручную»)
Подписываться на списки других пользователей
Подписываться на конкретный жанр (чтобы получать уведомления о выходе нового триллера, например)
Подписываться на ключевые слова – это что-то вроде меток (хочу узнавать, когда чему-то поставят метку «лакорн»)
Выражать свое мнение:

Выставлять фильму рейтинг
Писать отзывы на фильмы
Лайкать/дизлайкать отзывы других пользователей
Лайкать/дизлайкать указанный жанр фильма (ведь часто бывает, что заявленный, например, триллер в фильме так и не наступает)
Предлагать свой вариант жанра (из списка существующих)
Проставлять фильму ключевые слова/метки (новые или из списка уже добавленных),
Лайкать/дизлайкать метки, поставленные другими пользователями
Лайки/дизлайки позволяют вычислять в списках фильмов те, которые по мнению пользователей наиболее ярко выражают жанр или тему (по метке). В сочетании с возможностями разных подписок такое выражение мнения сильно облегчает подбор рекомендаций для конкретного пользователя и подбор похожих фильмов.

Для демонстрации работы скриптов с помощью сервиса filldb.info были сформированы абсолютно бессмысленные данные
