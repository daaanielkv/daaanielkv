# Даниил

**ML / DL** с фокусом на CV

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
<summary><b>Butterfly Classification</b> — сравнение архитектур и edge-деплой CV-модели</summary>
<br>
**Что сделал**
- Сравнил 4 backbone (MobileNetV3-Small, EfficientNet-B0, ResNet18, ResNet50) на классификации 50 классов бабочек не только по accuracy, но и по latency на CPU и размеру модели.
- Выбрал EfficientNet-B0 как компромисс accuracy/latency/размер, дообучил и экспортировал в ONNX.
- Заквантовал модель в INT8 и замерил реальный эффект: размер, latency, просадку accuracy

**Результат:** val accuracy 0.9889 (FP32) → 0.9657 (INT8, Δ −0.023), размер модели уменьшен в 3.15x

**Стек:** Python, PyTorch, torchvision, ONNX, onnxruntime

[Репозиторий](https://github.com/daaanielkv/butterfly-classification)
</details>

---

## Образование

**НИЯУ МИФИ**, Москва, бакалавриат 2027
Мехатроника и робототехника

**Цифровая кафедра МИФИ**, 2027
Прикладной анализ данных

**Deep Learning School**, 2025
Введение в DL/Computer Vision — диплом 2 степени
