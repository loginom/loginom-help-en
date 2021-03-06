# Сводка

Переменные, которые отдает порт *Сводка*, сведены в таблицу:

| Переменная (Метка) | Описание |
|:-------|:-------|
| Всего примеров | Общее число [примеров](https://wiki.loginom.ru/articles/training-sample.html), поданных на вход [модели](https://wiki.loginom.ru/articles/taught-model.html) |
| Всего отобранных примеров | Число примеров, используемое в модели |
| Примеров в [обучающем множестве](https://wiki.loginom.ru/articles/training-set.html) | Число примеров, на котором обучается модель |
| [Коэффициент детерминации](https://wiki.loginom.ru/articles/coefficient-of-determination.html) | Величина связи между переменными регрессионной модели (изменяется от 0 до 1) |
| [Скорректированный коэффициент детерминации](https://wiki.loginom.ru/articles/coefficient-determ-adj.html) | Величина связи между переменными регрессионной модели (изменяется от 0 до 1). Отличается от нескорректированного коэффициента детерминации тем, что скорректированный коэффициент может уменьшаться при введении в регрессионную модель переменных, не оказывающих существенного влияния на [зависимую переменную](https://wiki.loginom.ru/articles/output-variable.html). |
| [Число степеней свободы модели](https://wiki.loginom.ru/articles/degrees-of-freedom.html) | Число независимо варьируемых значений [признака](https://wiki.loginom.ru/articles/attribute.html) |
| [Информационный критерий Акаике](https://wiki.loginom.ru/articles/aic.html) | Критерий используется для сравнения моделей с разным числом параметров, когда требуется выбрать наилучший набор объясняющих переменных |
| [Информационный критерий Акаике скорректированный](https://wiki.loginom.ru/articles/aicc.html) | Модифицированный критерий Акаике, применяемый для [выборок](https://wiki.loginom.ru/articles/sample.html) малого размера, когда отношение числа содержащихся в ней примеров к числу параметров модели меньше 40 |
| [Информационный критерий Байеса](https://wiki.loginom.ru/articles/bic.html) | Критерий основан на использовании [функции правдоподобия](https://wiki.loginom.ru/articles/plausibility-function.html) и тесно связан с информационным критерием Акаике |
| [Информационный критерий Ханнана-Квина](https://wiki.loginom.ru/articles/hq.html) | Наряду с критерием Акаике и критерием Байеса, выдается в результатах оценки моделей с дискретными и ограниченными зависимыми переменными |
| [P-значение модели](https://wiki.loginom.ru/articles/p-value.html) | Оценка [точности](https://wiki.loginom.ru/articles/precision.html) модели. Представляет собой вероятность того, что значение проверочной статистики используемого критерия, вычисленное по выборке, превысит установленное p-значение. |