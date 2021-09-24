# Описание
Это бенчмарк скрипт для хакатона от Раййфайзенбанка по оценке коммерческой недвижимости
Бенчмарк состоит из:
* pyproject.toml - конфигурационный файл для менеджера пакетов poetry (https://python-poetry.org/) - в интернете есть много статей, посвященных ему (например https://habr.com/ru/post/455335/ и https://khashtamov.com/ru/python-poetry-dependency-management/)
* requirements.txt - стандартный requirements для pip
* train.py - скрипт, который обучает модель и сохраняет ее
* predict.py - скрипт, который делает предсказание на отложенной тестовой выборке

# Запуск
## Вариант с poetry
```sh
pip install poetry 
poetry  install  
```

## Запустить обучение
```sh
poetry run python3 train.py --train_data <path_to_train_data> --model_path <path_to_pickle_ml_model>
```

## Запустить предикт
```
poetry run python3 predict.py --model_path <path_to_pickled_model> --test_data <path_to_test_data> --output <path_to_output_csv_file>
```

## Data
https://doc-28-28-drive-data-export.googleusercontent.com/download/jpd2tpdd9nun7s8c317tt1rv10b0560d/b9jn056u6hs71mqd50i4k4pq68u40eed/1632505500000/5ebddcd9-8893-468c-ae52-0cf11d5a40b9/100327154754341176632/ADt3v-M0TJQfU4w63OmKEKZKGbGdFkFATXr2Fx32C0bLuaYNZjU11wWlyss8DZtkgFjebQKzDZTpJ4xl1QxYhctn0f5GZC4ajfV9mAnC17CNsz3acfYwH6pbwOM8DSJoWobcZYYo4qYh-kB1LpcIvrCaM8-e9cjwM7laWGR9sA7oqphOvVWYFV3AIan837sSvxOVnfpb-T8YgA_wPWCAhgqz8xy9ide2_V-Af1zdl2Klk-CJ9vv2Anur2lJOlKzEJ4qIG8OwJgt1cbpEqyeLNiibRW07sh-xUdPfb7iC1t0I6_ZUpspgiOtUufMMBGESx910bCz82VLD?nonce=8saa2uej1k9fo&user=100327154754341176632&authuser=0&hash=lvv6rou3opvo181a6ejo0sf7dod7k1ut
