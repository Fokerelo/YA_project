##  Построение модели определения стоимости автомобиля

**Задача*

Разработка системы рекомендации стоимости автомобиля на основе его описания

**Результат**

В итоге исследования у показатель RMSE у моделей LightGBM и CatBoost одинаковые - 1553,73. 
Исходя из требований заказчика:

качество предсказания;
время обучения модели;
время предсказания модели. Остается выбор только по двум критериям и тут CatBoots показывает лучшее время обучения 276 Ms против времени обучения у LightGBM 293 Ms.
А так же время предсказания у CatBoots всего лишь 1,126, тогда как у LightGBM время предсказание 1,15.
Стало быть нам подходит модель CatBoost с гиперпараметрами: 'depth': 10, 'learning_rate': 0.1

**Стек:**

Python
Pandas
lightgbm