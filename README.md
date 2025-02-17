# README

## Скрипт парсинга
**Файл:** `dual_gg.ipynb`

Python-скрипт для парсинга данных с сайта Kingfisher.kz. Этот инструмент позволяет быстро и эффективно собирать данные о товарах, обрабатывая ошибки и пропуская недоступные страницы. Сохранение данных происходит в удобном формате CSV.

## Структура репозитория

- **`dual_gg.ipynb`**: Скрипт для парсинга данных.
- **`my_postgres_project/`**: Папка с файлами для развертывания PostgreSQL.
- **`docker-compose.yml`**: Файл для запуска PostgreSQL через Docker.
- **`dual_db.ipynb`**: SQL-скрипт для создания таблицы и загрузки данных в PostgreSQL.
- **`dual_Analysis.ipynb`**: Скрипт анализа данных с визуализациями.
- **`kingfisher_data.csv`**: CSV-файл с собранными данными.
- **`kingfisher_data2.csv`**: Дополнительный CSV-файл с данными.
- **`README.md`**: Инструкция по запуску проекта.

## Описание
Этот проект создан для автоматизации процесса сбора, обработки и анализа данных с сайта Kingfisher.kz. С помощью скриптов можно собрать информацию о товарах, загрузить её в базу данных PostgreSQL и провести глубокий анализ с визуализацией результатов.

## Возможности
- Парсинг данных из категорий:
  - Рыба
  - Икра
  - Мясо
  - Антипасти
  - Бакалея
  - Снеки и орехи
  - Масло
  - Сыры
- Автоматическое сохранение данных в CSV-файл.
- Поддержка PostgreSQL для хранения данных.
- Полный анализ с использованием Python-библиотек.

## Требования
- Python версии 3.8+
- Необходимые библиотеки:
  - `requests`
  - `beautifulsoup4`
  - `pandas`
  - `matplotlib`
  - `seaborn`
- Docker и Docker Compose

Установить библиотеки можно командой:
```bash
pip install requests beautifulsoup4 pandas matplotlib seaborn
```

## Инструкция по запуску

### Этап 1: Парсинг данных
1. Откройте файл `dual_gg.ipynb` в Jupyter Notebook или другой среде.
2. Выполните ячейки скрипта.
3. После выполнения, данные будут сохранены в файлы `kingfisher_data.csv` и `kingfisher_data2.csv`.

### Этап 2: Загрузка данных в PostgreSQL
1. Разверните PostgreSQL через Docker:
   ```bash
   docker-compose up -d
   ```
2. Используйте файл `dual_db.ipynb` для создания таблиц и загрузки данных в базу:
   - Выполните ячейки для создания структуры таблиц.
   - Загрузите данные из файлов CSV в базу данных.

### Этап 3: Анализ данных
1. Откройте файл `dual_Analysis.ipynb` в Jupyter Notebook.
2. Выполните скрипт для построения графиков и анализа данных.
3. Графики и результаты анализа будут отображены и сохранены.

## Формат данных
- **Название продукта**: Название товара.
- **Категория продукта**: Категория, к которой относится товар.
- **Цена продукта**: Цена товара (в числовом формате).
- **Город**: Локация товара (по умолчанию "Астана").

## Выводы
- Проект позволяет полностью автоматизировать процесс сбора и анализа данных.
- Выявлены ключевые тенденции по категориям товаров и ценам на сайте Kingfisher.kz.
- Результаты визуализированы для лучшего понимания.

---

**Автор:** Нурсеит Амир  
**Группа:** BDA-2306

