# Квакин Даниил

**ML / CV**

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

- Спроектировал пайплайн из трёх компонентов: YOLO для детекции полос, классическое CV для предобработки изображений, 1D U-Net для сегментации профилей интенсивности
- Оптимизировал модель под инференс на NPU RK3588 через RKNN Toolkit
- Развернул решение на Orange Pi 5 (обработка изображений на edge-устройстве в реальном времени,
  без облака и без выделенного GPU)

**Результат**

ROC-AUC 0.966 на тестовой выборке.

**Стек:** Python, PyTorch, OpenCV, YOLOv8, RKNN Toolkit, Orange Pi 5.

</details>

---

## Собственные проекты

<details>
<summary><b>Butterfly Classification</b>. Задача сравнения архитектур и edge-деплой CV-модели</summary>
<br>
  
**Что сделал**

- Сравнил 4 backbone (MobileNetV3-Small, EfficientNet-B0, ResNet18, ResNet50) на классификации 50 классов изображений
- Заквантовал модель в INT8 и замерил параметры (размер, latency, просадку accuracy)

**Результат:** val accuracy 0.9889 (для FP32) | 0.9657 (INT8), размер модели уменьшен в 3.15 раз

**Стек:** Python, PyTorch, torchvision, ONNX, onnxruntime

[Репозиторий](https://github.com/daaanielkv/butterfly-classification)
</details>

<details>
<summary><b>Rotation Detector</b>. Задача определения переворота текстового кропа на 180</summary>
<br>

**Что сделал**

- Сгенерировал полностью синтетический датасет: текст (слова, цены, телефоны, даты, коды) разными шрифтами на реалистичных фонах с аугментациями
- Учёл ротационную симметрию символов и строк (такие примеры размечены как неопределённые (label = 0.5), чтобы не шуметь в обучении)
- Сравнил 5 лёгких backbone из `timm` (MobileNetV3-Small, MobileNetV3-Large, ResNet18, EfficientNet-B0, MobileViTv2-050) по Brier score и CPU-latency

**Результат:** лучший баланс качества/скорости на ResNet18

**Стек:** Python, PyTorch, timm, OpenCV

[Репозиторий](https://github.com/daaanielkv//text-orientation)
</details>

## Образование

**НИЯУ МИФИ**, Москва, бакалавриат 2027
Мехатроника и робототехника

**Цифровая кафедра МИФИ**, 2027
Прикладной анализ данных

**Deep Learning School**, 2025
Введение в DL/Computer Vision — диплом 2 степени
