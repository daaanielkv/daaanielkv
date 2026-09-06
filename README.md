# Даниил

**ML / DL** · фокус на computer vision и edge-деплое — довожу модели до работы на NPU без GPU-сервера.

[GitHub](https://github.com/daaanielkv) ·
[Telegram](https://t.me/danbackyardtg) ·
[Почта](mailto:daniilkvakin@gmail.com)

---

## Содержание

- [Стек](#стек)
- [Опыт работы](#опыт-работы)
- [Собственные проекты](#собственные-проекты)
- [Образование](#образование)

---

## Стек

| Направление | Технологии |
| --- | --- |
| **Computer Vision** | OpenCV, YOLO, классический CV, PyTorch |
| **ML / DS** | scikit-learn, pandas, NumPy, Transformers, fine-tuning |
| **Retrieval** | char-ngram, TF-IDF, kNN, эмбеддинги |
| **Данные и автоматизация** | PostgreSQL |

---

## Опыт работы

<details>
<summary><b>ИТЭЛМА</b> — стажёр-разработчик</summary>

<br>

Разработка CV-пайплайна **GelDoc** для анализа изображений гель-электрофореза с деплоем на edge-устройство.

**Что сделал**

- Спроектировал пайплайн из трёх компонентов: YOLO для детекции полос, классическое CV
  для предобработки изображений, 1D U-Net для сегментации профилей интенсивности.
- Оптимизировал модель под инференс на NPU RK3588 через RKNN Toolkit.
- Развернул решение на Orange Pi 5: обработка изображений на edge-устройстве в реальном времени,
  без облака и без выделенного GPU.

**Результат**

ROC-AUC 0.966 на тестовой выборке.

**Стек:** Python, PyTorch, OpenCV, YOLOv8, RKNN Toolkit, Orange Pi 5.

</details>

---

## Собственные проекты

<details>
<summary><b>Retail CV Analytics</b> — трекинг покупателей в ритейле на edge-устройствах</summary>

<br>

Пайплайн для анализа поведения покупателей в торговых точках, часть исследования рынка
edge CV analytics для российского retail SMB-сегмента.

**Что сделал**

- Собрал пайплайн детекции и трекинга людей: YOLOv8/YOLO26 + BoT-SORT + ReID.
- Обучил и протестировал на CrowdHuman с прицелом на деплой на edge-устройства.
- Провёл предметное исследование рынка: конкуренты, вертикали, потенциальные ниши.

**Стек:** Python, YOLOv8/YOLO26, BoT-SORT, ReID, CrowdHuman.

</details>

<details>
<summary><b>Avito RAG</b> — гибридный retrieval-пайплайн, MAP@10 ≈ 0.437</summary>

<br>

**Что сделал**

- Реализовал гибридный поиск: BM25 + dense retrieval.

**Результат:** MAP@10 ≈ 0.437.

**Стек:** Python, BM25, dense retrieval.

</details>

<details>
<summary><b>RTO Forecasting</b> — прогнозирование для Pyaterochka, MAPE ~7%</summary>

<br>

**Что сделал**

- Построил пайплайн прогнозирования на LightGBM/CatBoost.

**Результат:** MAPE ~7%.

**Стек:** Python, LightGBM, CatBoost.

</details>

<details>
<summary><b>UEBA Anomaly Detection</b> — автоэнкодер для детекции аномального поведения</summary>

<br>

**Что сделал**

- Реализовал автоэнкодер на PyTorch для детекции аномалий в поведенческих данных.

**Результат:** ROC-AUC ~0.966.

**Стек:** Python, PyTorch.

</details>

<details>
<summary><b>IAEA Docs Scraper</b> — сбор публикаций МАГАТЭ</summary>

<br>

**Что сделал**

- Собрал многоэтапный пайплайн скрейпинга на Playwright с автоматизацией через Makefile.

**Стек:** Python, Playwright, Makefile.

[Репозиторий](https://github.com/plotv/IAEA_doc)

</details>

---

## Образование

**НИЯУ МИФИ**, Москва, бакалавриат 2027
Мехатроника и робототехника

**Цифровая кафедра МИФИ**, 2027
Прикладной анализ данных

**Deep Learning School**, 2025
Введение в DL/Computer Vision — диплом 2 степени
