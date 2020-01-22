# Сервис по поиску тренера

## Структура проекта
В каждой папке находится свой readme файл с более подробным описанием

**Верхнеуровневое описание:**
 - **DataAggregator** - Каталог со всем исходным кодом приложения
 - **DataReport** - Каталог с файлами общего Django-проекта DataReport, внутри которого создано приложение DataAggregator
 - **db.sqlite3** - Дефолтная SQLite база фреймфорка
 - **manage.py** - Дефолтный скрипт фреймворка
 
## Настройки приложения
Сервис умеет работать с даннными в двух режимах:
1. Загружать данные из csv файла
2. Получать данные через API портала открытых данных (data.mos.ru)

Настройки находятся в файле apps.py в каталоге DataAggregator:
- **DATA_LOAD_METHOD** - Способ загрузки данных. Принимает 1 из 2 возможных значений: API или CSV
- **DATA_LOAD_CSV_PARAMS** - Настройки для извлечения данных из csv-файла
- **DATA_LOAD_API_PARAMS** - Настройки для подключения к внешнему API
- **DATA_LOAD_MAX_RECORDS** - Максимальное количество извлекаемых записей

## Инструкция по запуску проекта
### Windows
1. Установить Python 3 (https://www.python.org/downloads/)
2. Установить Django:
```
pip install django
```
3. Скопировать репозиторий (при наличии установленного git) или просто скачать файлы из репозитория:
```
git clone https://github.com/SergeyMerkudinov/DataReport.git
```
4. Перейти в папку с проектом и запустить сервер в командной строке:
```
python manage.py runserver
```
5. Открыть браузер и перейти по адресу localhost:8000.
