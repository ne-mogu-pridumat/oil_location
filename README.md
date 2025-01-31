# Прогнозирование локаций для нефтяной скважины 

**Цель**
Определить регион, где бурить новую нефтяную скважину.

**Задача**
Построить модель для определения региона, где добыча принесёт наибольшую прибыль

**Описание данных**
В данном проекте 3 датасета: `geo_data_0.csv`, `geo_data_1.csv`, `geo_data_2.csv` со следующими признакми

- `id` — уникальный идентификатор скважины;
- `f0`, `f1`, `f2` — три признака точек (неважно, что они означают, но сами признаки значимы);
- `product` — объём запасов в скважине (тыс. баррелей).

# Общий вывод по проекту

В этом проекте требуется определить, в каком регионе лучше всего бурить новую нефтяную скважину. Были получены датасеты с 3 регионами, которые содержат три признака точек (f0, f1, f2) и объём запасов в скважине (product) (id не берем в расчет, т.к. для иследования он не пригодился и был удален). Далее перечислю ключевые краткие выводы по проекту:

- В ходе исследования данных было установлено, что f2 имеет существенное влияние на объем запасов product во 2 регионе (geo_data_1).
- Была обучена модель с помощью линейной регрессии и выявлены метрики RMSE и R2. Лучше всего показал 2 (geo_data_1) регион с показателями: Средний объем предсказанного сырья 68.73, RMSE = 0.89, R^2 = 0.99962.  Хотб она предсказывает меньший объем сырья, но точность модели гораздо выше.
- Была получена точка безубыточности в размере 111.11. Ближе к точки безубыточности находится средний запас в 3 регионе (geo_data_2) с результатом -16.23.
- Наибольшую прибыльность и минимальный сроку окупаемости было получено в 1 регионе (geo_data_0) - 3320826043 и 36 месяцев.
- Минимальный риск вложения (всего 1%) показал 2 регион (geo_data_1) со значениями средней прибыли в 461157248.

Таким образом, регион 2 (geo_data_1) представляет собой оптимальный выбор с учетом сочетания высокой прибыльности, минимального риска и точности прогнозирования.
