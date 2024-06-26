# Отбор признаков. Кластеризация данных

## Описание проекта

Проект выполнен в рамках курса "Практический Machine Learning" (https://stepik.org/course/125501/syllabus).

В рамках проекта рассмотрен ряд методов усовершенстования модели регрессии (на примере дерева решений):

- логарифмирование целевой переменной;

- введение полиномиальных признаков;

- стандартизация и отбор признаков;

- кодирование категориальных признаков.

Также показаны возможности применения кластеризации в анализе данных и определении статистических характеритик данных, входящих в кластеры.

Выполнение проекта осуществлялось на базе датасета, содержащего информацию о поездках в такси Нью-Йорка (https://www.dropbox.com/s/glmbcyopi24m2ni/final_project_data.csv?dl=1).

## Этапы выполнения проекта

1. Предобработка данных: обработка пропущенных значений, выделение отдельных признаков из композиций признаков.

2. Предварительный анализ данных, проверка на наличие пропусков, выбросов, построение и анализ характеристик распределений признаков.

3. Построение baseline модели решающего дерева. Оценка качества модели на тестовом датасете. Определение наиболее важных признаков согласно baseline модели.

4. Применение различных подходов для улучшения качества baseline модели. Оценка качества на тестовом датасете.

5. Кластеризация данных, анализ характеристик кластеров 

## Результаты и выводы

Предварительный анализ данных показал, что наибольшее количество заказов такси наблюдается в весеннее время. Пиковые часы - в конце дня (после работы и вечернее время). Установлено наличие выбросов в данных (отдаленных точек посадки/высадки пассажиров)

Построена baseline модель решающего дерева, которая на тестовой выборке показала R2-score, равный 0.5. Построена визуализация важности признаков на основе данной модели. Показано, что наибольший вес при прогнозировании стоимости поездки имеют долгота высадки и посадки пассажира

Применен ряд подходов для улучшения качества baseline модели:

- логарифмирование целевой переменной

- введение полиномиальных признаков

- стандартизация и отбор признаков

- кодирование категориальных признаков

Все отмеченные подходы позволили улучшить качество baseline модели. Наиболее эффективным оказалось введени полиномиальных признаков, что позволило увеличить R2-score до 0.7.

На датасете, очищенном от выбросов (исключены отдаленные пункты высадки пассажиров), выполнена кластеризация точек высадки пассажиров. Выделен кластер с наиболее высокой стоимостью поездки. Выполнена кластеризация данного кластера на 3 дополнительных кластера, показана возможность вычисления их географических центров. Таким образом проиллюстрирована возможность применения кластеризации, например, для определения потенциально выгодных клиентов (по району конечной точки маршрута).

Ноутбук проекта доступен по ссылке: ["Отбор признаков. Кластеризация данных"](https://github.com/ElenaNKn/projects/blob/master/project_clustering_pipelines_feature_selection/project.ipynb)