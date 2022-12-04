# cs_tournament_test
Кросс валидировал разные конфигурации фичей с помощью катбуста на 8 фолдах, подбирал гиперпараметры с помощью оптюны.

Итоговые модели:

## Модель 1 prediction_1.csv
Просто на train.csv без добавления фичей.  
На кросс валидации дает самый большой рок аук ~.72

## Модель 2 prediction_2.csv
train.csv + разность сумм общего кол-ва смертей `total_deaths` 1ой команды и второй.  
Это сочетание дает самый высокий рокаук самого проблемного фолда.

## Модель 3 prediction_3.csv
train.csv + разность сумм:
* headshots	
* total_deaths	
* kd_ratio	
* total_opening_kills	
* total_opening_deaths

Эти фичи были выбраны, потому что они давали рок аук худшего фолда больше .65
