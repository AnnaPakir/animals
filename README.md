# Разработка сверточной нейронной сети

Код [link](https://github.com/AnnaPakir/animals/blob/main/animals.ipynb)

Отчет 

В данной работе был произведен эксперимент по созданию сверточной нейронной сети для многоклассовой классификации изображений.

Ссылка на данные в Kaggle: [link](https://www.kaggle.com/datasets/alessiocorrado99/animals10/data)

![plot](https://github.com/AnnaPakir/animals/blob/main/animals_png.png)

В результате были созданы три полносвязные сети. Сети обучалась на 10 эпохах:

| Модель  | Время обучения | Количество сверточных слоев | Особенности | Accuracy |
| --- | --- | --- | --- | --- | 
| model_base | 4359 | 0| Только полносвязные слои | 0.18 |
| model_1 | 17436 | 2| Добавлены сверточные слои | 0.50 |
| model_2 | 19180 | 4| Добавлен dropout  и нормализация | 0.61 % |
| model_2 | 19180 | 4| Добавлена  l2 регуляризацию, разные значения dropout на разных слоях | 0.45 % |

Был проанализирован и зафиксирован процесс обучения каждой нейронной сети. Последняя модель показала минимальное переобучение, но ей не хватило 10 эпох для обучения. Было провелено обучении ее на 50 эпохах, но добавлена регуляризация эпох и также постепенное уменьшение шага обучения в процессе обучения. В итоге модель подняла метрику как на тренировочных, так и на валидационных данных до 0.76.

![plot](https://github.com/AnnaPakir/animals/blob/main/model_cnn.png)

Данная модель может быть доработана посредством доработки обучабщей выборки: аугументация данных, сравнения эксземпляров эпох и т.д. 
