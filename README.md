# Final-project
# Проект №3: Анализ логов

## Общая задача
Создание скрипта для формирования витрины на основе логов web-сайта.

## Подробное описание задачи
Задача включает разработку скрипта для формирования витрины, содержащей следующие данные:
1. Суррогатный ключ устройства
2. Название устройства
3. Количество пользователей
4. Доля пользователей данного устройства от общего числа пользователей
5. Количество совершенных действий для данного устройства
6. Доля совершенных действий с данного устройства относительно других устройств
7. Список из 5 самых популярных браузеров, используемых на данном устройстве различными пользователями, с указанием доли использования для данного браузера относительно остальных браузеров
8. Количество ответов сервера, отличных от 200 на данном устройстве
9. Для каждого из ответов сервера, отличных от 200, сформировать поле, в котором будет содержаться количество ответов данного типа

## Использованные источники
Для выполнения задачи использовались csv-файл и log-файл. Оба источника данных были обработаны, а затем объединены в один датафрейм.

## Содержание работы
1. Установка необходимых пакетов
2. Импорт и анализ log-файла
3. Импорт и анализ csv-файла
4. Объединение двух источников данных
5. Выполнение скриптов для формирования витрины
6. Создание финального датафрейма
7. Пример использования Apache Airflow для автоматического запуска скрипта

## Работа с использованием Apache Spark в Google Colab
Работа велась с использованием Apache Spark в среде Google Colab, что обеспечило масштабируемость и эффективную работу с большим объемом данных.
## Работа с использованием Apache Airflow
Apache Airflow использовался с целью автоматического запуска разработанного в ходе текущего проекта скрипта (my_dag.py). 
Выполнение указанного скрипта запланировано на понедельник каждой недели, начиная с 25 декабря 2023 года, что можно увидеть из фрагмента скрипта: 
default_args = {
    'owner': 'airflow',
    'start_date': datetime(2023, 12, 25),
    'retry_delay': timedelta(minutes=5),
    'schedule_interval': '0 0 * * MON',
}
## Инструкция по развертыванию. 
1. Скачать файл со скриптом "Final_project_.ipynb"на локальную машину.
2. Загрузить указанный скрипт в Google Drive.
3. Поделючиться к среде выполнения.
4. Перезапустить среду выполнения и выполнить код всех ячеек в блокноте.
   
### Автор проекта: [Петрунина Анастасия]
Контактная информация: [nastya_zhara@inbox.ru]
