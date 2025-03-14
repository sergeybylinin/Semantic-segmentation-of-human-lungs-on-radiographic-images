# Сегментации легкие человека на радиографическом снимке

### Цель проекта:
Разработка модели для автоматической семантической сегментации легких на радиографических снимках (рентгенограммах) с целью улучшения диагностики заболеваний дыхательной системы, таких как пневмония, COVID-19, туберкулез и другие патологии.

### Что было сделано:
* Данные kagle COVID-19 Radiography Database https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database
* Проведена предварительная обработка данных: нормализация, аугментация данных (повороты, отражения) для увеличения разнообразия данных.

### Выбор архитектуры модели:

Для задачи семантической сегментации выбрана архитектура U-Net++, которая хорошо зарекомендовала себя в медицинской визуализации благодаря своей способности работать с ограниченным количеством данных и высокой точностью.

### Обучение модели:

Модель обучалась на размеченных данных с использованием функции потерь binary_crossentropy, которая хорошо подходят для задач сегментации.
Для оптимизации использовался Adam
Проведено обучение с использованием GPU для ускорения процесса.

### Оценка и валидация:

Для оценки качества модели использовалась метрика accuracy.
Модель тестировалась на независимом тестовом наборе данных для оценки обобщающей способности.

### Интерпретация результатов:

Визуализированы результаты сегментации для анализа ошибок и улучшения модели.

### Для чего это нужно:
* Автоматизация диагностики: Модель позволяет автоматически выделять область легких на снимках, что упрощает работу врачей-рентгенологов и ускоряет процесс диагностики.
* Обнаружение патологий: Сегментация легких является первым шагом для дальнейшего анализа, например, обнаружения очагов пневмонии или других заболеваний.
* Снижение нагрузки на врачей: Автоматизация рутинных задач позволяет врачам сосредоточиться на более сложных случаях.

### Трудности и боли, которые были решены:
Недостаток размеченных данных. Медицинские данные часто ограничены из-за конфиденциальности и сложности разметки. Решение: использование аугментации данных.

### Интерпретируемость модели:
В медицине важно, чтобы модель не только была точной, но и понятной для врачей. Решение: визуализация результатов и объяснение предсказаний модели.

### Итог:
Проект успешно решил задачу автоматической сегментации легких на радиографических снимках, что может быть использовано в медицинской практике для улучшения диагностики и снижения нагрузки на врачей. Модель показала высокую точность и устойчивость к различным патологиям, что делает ее применимой в реальных условиях.
