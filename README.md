# ⚽ Прогнозирование исходов футбольных матчей с использованием алгоритмов машинного обучения

## 📌 Описание

Этот проект представляет собой реализацию системы для прогнозирования исходов футбольных матчей на основе алгоритмов машинного обучения. Основная цель — анализировать исторические данные и статистику матчей Английской Премьер-Лиги и предсказывать победу, ничью или поражение в будущих играх. Исследование охватывает сбор данных, предварительную обработку, построение и обучение моделей, оценку точности, а также предсказание итоговой таблицы сезона 2023–2024.

Проект выполнен в рамках курсовой работы студента 2 курса механико-математического факультета БГУ — Дмитрия Урбановича.

## 🎯 Цели проекта

- Исследовать методы анализа и прогнозирования спортивных событий.
- Сравнить эффективность различных моделей машинного обучения.
- Применить алгоритмы к реальным данным по матчам Английской Премьер-Лиги.
- Определить точность моделей и их применимость к спортивной аналитике.
- Построить прогноз на весь сезон 2023/24 и определить потенциального чемпиона.

## 🧠 Используемые алгоритмы

- **Логистическая регрессия**
- **Случайный лес (Random Forest)**
- **Решающие деревья (Decision Tree)**
- **Наивный байесовский классификатор (Naive Bayes)**
- **Градиентный бустинг (XGBoost)**

## 🗃 Источники данных

- Статистика с сайта [fbref.com](https://fbref.com/en/comps/9/Premier-League-Stats)
- Данные охватывают 6 сезонов (с 2018 по 2024 гг.)
- Сбор данных с использованием `requests`, `BeautifulSoup`, `pandas`

## ⚙️ Стек технологий

- Python 3
- Pandas, NumPy, Scikit-learn, XGBoost
- BeautifulSoup (парсинг)
- Matplotlib / Seaborn (визуализация)
- Jupyter Notebook / Google Colab

## 🛠️ Этапы реализации

### 1. Сбор и предобработка данных
- Парсинг данных о матчах с fbref.com
- Очистка данных, кодирование признаков, генерация целевой переменной (`target`)
- Формирование обучающей и тестовой выборки (по дате)

### 2. Обучение моделей
- Реализация и обучение различных алгоритмов
- Использование метрик `accuracy`, `precision` для оценки качества
- Построение матриц ошибок и сравнительных диаграмм

### 3. Повышение качества модели
- Добавление новых признаков: капитан, расстановка, посещаемость
- Вычисление скользящих средних значений по команде
- Повторное обучение и анализ прироста точности

### 4. Прогнозирование таблицы сезона
- Подсчёт предсказанных очков для каждой команды
- Сравнение с реальной таблицей Премьер-Лиги
- Определение наиболее точной модели и чемпиона по прогнозу

## 📊 Результаты

- **Наиболее точная модель**: Логистическая регрессия (~57.3%) и Наивный Байес (~58.7%)
- **Прогноз показал**: Лидерство Arsenal, Man City и Liverpool
- **Реальные vs Предсказанные очки**: Предсказания имели высокое соответствие с реальными результатами, особенно в нижней части таблицы (Burnley, Sheffield Utd, Luton Town).

## 📈 Визуализация и анализ

- Таблицы сопряжённости
- Сравнительные графики моделей
- Таблицы очков: реальные vs предсказанные
- Диаграммы важности признаков

## 📚 Полезные ресурсы

- [Scikit-learn documentation](https://scikit-learn.org/stable/)
- [Pandas documentation](https://pandas.pydata.org/)
- [Hands-On Machine Learning (Aurélien Géron)](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/)
- [Colab-ноутбук проекта](https://colab.research.google.com/drive/143_EnIE0xN0C9fq8XFx2YLv6tf78vi8c?usp=sharing)

## 🧠 Выводы

- Методы машинного обучения применимы к спортивному анализу и способны выявлять закономерности в данных.
- Даже простые модели, такие как логистическая регрессия и Naive Bayes, показывают хорошие результаты.
- Важно правильно отбирать и обрабатывать признаки.
- Точные прогнозы требуют учёта большого числа внешних факторов (травмы, состав, стратегия и др.).

## ✅ Перспективы развития

- Подключение дополнительных источников (новости, составы, травмы)
- Использование нейронных сетей (LSTM для временных рядов)
- Расширение на другие чемпионаты и виды спорта
- Разработка веб-интерфейса для ввода данных и получения прогноза
