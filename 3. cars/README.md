# Определение стоимости автомобилей
Сервис по продаже автомобилей с пробегом разрабатывает приложение для привлечения новых клиентов. Суть приложения заключается в том, чтобы покупатель мог быстро узнать рыночную стоимость своего автомобиля. В нашем распоряжении имеются исторические данные сервиса: технические характеристики, комплектации и цены автомобилей. На основе этих данных необходимо разработать модель, способную определить стоимость автомобиля

# Вывод 
Были обучены следующие модели: DecisionTreeRegressor, LightGBM и CatBoost. По итогам обучения лучшей оказалась модель LightGBM, также прошедшая проверку на адекватность, совершённую с помощью константной модели DummyRegressor:
- `Метрика RMSE модели LightGBM на тренировочной выборке`: 1602.9530708972213
- `Метрика RMSE модели LightGBM на тестовой выборке`: 1586.6515978729988
- `Метрика RMSE для модели DummyRegressor`: 4642.107553

Каждая из трёх обученных моделей отвечает основному требованию задачи — чтобы метрика RMSE была меньше 2500. Итоговый выбор модели основан на соблюдении баланса качества и скорости модели. Так, самой быстрой по скорости обучения является модель LightGBM, по качеству она занимает второе место среди двух других моделей. Самая маленькая скорость обучения получилась у CatBoost, посередине — DecisionTreeRegressor, однако качество CatBoost относительно двух других моделей является самым высоким и надёжным