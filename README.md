# Technopark-VK-ML-cost-prediction
## Description
Участникам предоставлен набор данных объявлений о продаже недвижимости в некотором волшебном городе N. Задача - предсказать цену недвижимости по содержанию объявления.
## Evaluation
Метрика данного соревнования mean absolute error [MAE]

Балл рассчитывается как обратная величина метрике: score = 1 / (1 + MAE)

Разбиение на Train/Test выполнено по времени объявления.\
Разбиение тестового набора на Public/Private выполнено случайным образом в пропорции 30/70% соответственно.

## Файлы
_preproc.ipynb_ - предобработка кода с изолированной заменной null'ов, работа с датой с помощью регулярных выражений\
_first_try.ipynb_ - старый основной файл, но в нём слишком большой вывод ячейки => _first_try_removed.ipynb_\
**_first_try_removed.ipynb_** - основной файл, со всеми этапами предобработки данных, добавлением новых фич, нормализацией и работой с категориальными фичами, подбором гиперпараметров и последующим predict'ом, работа с датой через datetime64[ns]\
_remove_output.py_ - доработанный скрипт из просторов интернета для удаления вывода ячейки\
_KAN_try.ipynb_ - начал разбиравться с новой архитектурой, не успел(

## Данные
_StandardScaler_CatBoostRegressor_1_000_000_new_features_v2.csv_ - результат работы CatBoostRegressor для test с 1_000_000 итераций, новыми фичами\
_X2_CatBoostRegressor_1_000_000_new_features_v2.csv_ - тоже самое, опираясь на файл выше\
_trainStandardScaler_CatBoostRegressor_1_000_000_new_features_v2.csv_ - тоже самое, для train\
_train_X2_CatBoostRegressor_1_000_000_new_features_v2.csv_ - тоже самое, опираясь на файл выше\
_train_fillna_mean.csv_ - заполнение null'ов по столбцам

_train.csv_\
_test.csv_\
_sample_submission.csv_
