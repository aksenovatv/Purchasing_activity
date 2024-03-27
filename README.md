# Предсказание вероятности снижения покупательской активности

**Цель исследования:** Разработать решение, которое позволит персонализировать предложения постоянным клиентам, чтобы увеличить их покупательскую активность.

**Описание данных:** В нашем распоряжеии 4 датасета.

1. Файл `market_file.csv` содержит данные о поведении покупателя на сайте, о коммуникациях с покупателем и его продуктовом поведении:\
`id` — номер покупателя в корпоративной базе данных.\
`Покупательская активность` — рассчитанный класс покупательской активности (целевой признак): «снизилась» или «прежний уровень».\
`Тип сервиса` — уровень сервиса, например «премиум» и «стандарт».\
`Разрешить сообщать` — информация о том, можно ли присылать покупателю дополнительные предложения о товаре. Согласие на это даёт покупатель.\
`Маркет_актив_6_мес` — среднемесячное значение маркетинговых коммуникаций компании, которое приходилось на покупателя за последние 6 месяцев. Это значение показывает, какое число рассылок, звонков, показов рекламы и прочего приходилось на клиента.\
`Маркет_актив_тек_мес` — количество маркетинговых коммуникаций в текущем месяце.\
`Длительность` — значение, которое показывает, сколько дней прошло с момента регистрации покупателя на сайте.\
`Акционные_покупки` — среднемесячная доля покупок по акции от общего числа покупок за последние 6 месяцев.\
`Популярная_категория` — самая популярная категория товаров у покупателя за последние 6 месяцев.\
`Средний_просмотр_категорий_за_визит` — показывает, сколько в среднем категорий покупатель просмотрел за визит в течение последнего месяца.\
`Неоплаченные_продукты_штук_квартал` — общее число неоплаченных товаров в корзине за последние 3 месяца.\
`Ошибка_сервиса` — число сбоев, которые коснулись покупателя во время посещения сайта.\
`Страниц_за_визит` — среднее количество страниц, которые просмотрел покупатель за один визит на сайт за последние 3 месяца.


2. Файл `market_money.csv` с данными о выручке, которую получает магазин с покупателя, то есть сколько покупатель всего потратил за период взаимодействия с сайтом:\
`id` — номер покупателя в корпоративной базе данных.\
`Период` — название периода, во время которого зафиксирована выручка. Например, `'текущий_месяц'` или `'предыдущий_месяц'`.\
`Выручка` — сумма выручки за период.


3. Файл `market_time.csv` с данными о времени (в минутах), которое покупатель провёл на сайте в течение периода.\
`id` — номер покупателя в корпоративной базе данных.\
`Период` — название периода, во время которого зафиксировано общее время.\
`минут` — значение времени, проведённого на сайте, в минутах.


4. Файл `money.csv` с данными о среднемесячной прибыли покупателя за последние 3 месяца: какую прибыль получает магазин от продаж каждому покупателю.\
`id` — номер покупателя в корпоративной базе данных.\
`Прибыль` — значение прибыли.