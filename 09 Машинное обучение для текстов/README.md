# Определение токсичности комментариев

## Задача

Обучите модель классифицировать комментарии на позитивные и негативные

## Данные

Набор данных с разметкой о токсичности правок.

## Библиотеки

- pandas
- numpy
- matplotlib.pyplot
- statsmodels
- sklearn
- lightgbm
- re
- transformers
- nltk
- seaborn

## Вывод

При расчете метрики качества F1 получили следующие результаты:
- Метрика качества F1 у LogisticRegression - TF-IDF выше чем LogisticRegression - CountVectorizer
- Метрика качества F1 без лемматизации текста выше чем с лемматизацией текста
- LogisticRegression - TF-IDF без лемматизации текста на тестовой выборке показал метрику качества F1 выше 0.75.
- Метрика качества F1 у LogisticRegression лучше чем DecisionTreeClassifier
- DecisionTreeClassifier метрика качества F1 ниже 0.75 



