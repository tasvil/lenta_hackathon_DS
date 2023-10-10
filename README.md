# lenta_hackathon_DS
Hackathon by Lenta and Practicum on Time Series

Разработана регрессионная модель для прогноза спроса на товары собственного производства Ленты на 14 дней. Применена метрика WAPE на уровне товаров, магазинов и дней.

В ходе работы выполнены следующие шаги:

- Проведен обзор данных, их объединение и предобработка, включая исправление отрицательных значений и удаление аномалий.

- Проведен исследовательский анализ данных, выявлены особенности продаж по магазинам и группам товаров, анализ временных рядов, а также изучена корреляция признаков.

- Созданы новые признаки, включая лаги и скользящие средние, учитывая особенности задачи прогнозирования на 14 дней. Также добавлены признаки, связанные с праздниками и сопутствующими товарами.

- Проведен анализ возможности разделения данных на группы. Оптимальным оказался подход, включающий разделение на ТОП-50 товаров и остальные.

- Подобраны и обучены модели регрессии (LGBMRegressor, CatBoost, и LinearRegression) с учетом специфики временных рядов и с разбиением на группы. Для товаров без промоакций была обучена отдельная модель. Гиперпараметры подобраны с использованием оптимизации и поиска по сетке.

В результате работы достигнуты следующие результаты:

WAPE для группы 1 (ТОП-50 товаров) составил 0.38.
WAPE для группы 2 (Остальные товары) составил 0.444.
