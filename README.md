﻿# DiskProSila

![Титул (1)](https://github.com/user-attachments/assets/45e5c8b8-7905-4c83-beef-1ae6e00fc125)


Этот проект предназначен для предсказания отказов жестких дисков с использованием моделей машинного обучения. Основная цель проекта — предсказать вероятность отказа дисков в зависимости от различных факторов.

## Описание

Программа предоставляет функционал для:

1. **Обучения модели** на основе предоставленных данных.
2. **Предсказания** вероятности отказа дисков на основе обученной модели.
3. **Дообучения модели** на новых данных.

## Зависимости

- Python 3.x
- H2O
- pandas
- numpy
- scikit-learn

## Установка

Установите необходимые зависимости с помощью pip:

```bash
pip install h2o pandas numpy scikit-learn

Использование
Обучение модели
Чтобы обучить модель, используйте команду:

python failure_prediction.py --train_model --train_file path_to_train_file.csv --model_path path_to_save_model

--train_model: Запускает обучение модели.
--train_file: Путь к файлу с обучающими данными.
--model_path: Путь для сохранения модели.

Предсказание
Для выполнения предсказания используйте команду:
python failure_prediction.py --predict --model_path path_to_saved_model --data_file path_to_data_file.csv --output_file path_to_save_predictions.csv

--predict: Запускает предсказание.
--model_path: Путь к ранее сохраненной модели.
--data_file: Путь к файлу с данными для предсказания.
--output_file: Путь для сохранения предсказаний.
Дообучение модели
Для дообучения модели используйте команду:
python failure_prediction.py --retrain_model --model_path path_to_saved_model --new_data_file path_to_new_data_file.csv

--retrain_model: Запускает дообучение модели.
--model_path: Путь к ранее сохраненной модели.
--new_data_file: Путь к новому файлу с данными для дообучения.
Пример использования
python failure_prediction.py --train_model --train_file data/train_data.csv --model_path models/
python failure_prediction.py --predict --model_path models/ --data_file data/test_data.csv --output_file predictions.csv
python failure_prediction.py --retrain_model --model_path models/ --new_data_file data/new_train_data.csv

Логирование
Вывод программы сохраняется в файл output_log.txt.

Автор: Хакатонщики-3000

Лицензия
Этот проект лицензирован под лицензией MIT. Смотрите файл LICENSE для получения подробной информации.
