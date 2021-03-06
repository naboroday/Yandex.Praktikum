
# Определение температуры для выплавки стали

## Задача

Построить модель, которая по данным будет предсказывать температуру

## Данные

Показания с замерами

## Библиотеки

- pandas
- numpy
- matplotlib.pyplot
- sklearn
- catboost 
- lightgbm

## Отчет по проекту

**Результат по главе №1:**
- Проверили и проанализировалвали датасеты на пропуски и дубликаты
- Заменили время на тип данных Datetime
- Отбросили отрицательные значения реактивной мощности
- Расчитали и ввели признак `полная мощность` вместо активной и реактивной мощности из-за высокой корреляции между ними
- Определили в датасете data_temp, что партии с №2500 имеют один замер температуры
- Датасет data_wire_time не будет использоваться

**Результат по главе №2:**
- Отбросили номера партий больше 2500
- Отбросили промежуточные температуру и ввели `target - Last_temp` для обучения моделей
- Оставили только полную мощность
- Соединили таблицы в одну итоговую таблицу
- Разделили выборки на 30% тестовой выборки и 70% обучающей выборки
- Выполнили масштабирование признаков

**Результат по главе №3:**
- Лучшая модель по метрике МАЕ - `CatBoostRegressor` с показанием на тестовой выборке МАЕ=6.44
- Главным фактором при обучение моделей является `начальная температура`
- Предлагаю для производства определить оптимальный диапазон границ  `начальной температуры` и фиксировать причины нарушения границ (химический состав газа, работу бригад и т.д.)
- Можно разрабатывать энергосберегательные мероприятия с помощью проверок гипотез или обучения моделей для контроля оптимального диапазона границ `начальной температуры`
- На обучине моделей никак не влиют следующие факторы, на которые необходимо обратить внимание:
    - № Wire - `5, 7, 8, 9`
    - № Bulk - `2, 7, 8, 9, 13`




