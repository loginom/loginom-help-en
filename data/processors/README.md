# Обработка

## Основные понятия

**Сценарий** - последовательность действий, которые необходимо провести для анализа данных. Сценарий обработки представляет собой комбинацию узлов обработки данных, настраиваемую пользователем для решения конкретной задачи.

Последовательность обработки задается соединением выхода предыдущего узла сценария со входом последующего. Входом и выходом узла являются **входные** и **выходные порты**.

![](../quick-start/readme-1.png)

*Пример сценария*

**Узел** сценария выполняет отдельную операцию над данными. Перечень возможных операций представлен палитрой готовых **компонентов**. Таким образом, **компонент** является прообразом или шаблоном будущего узла сценария. Для того, чтобы создать узел сценария, выполняющий нужную операцию над данными, необходимо мышью перенести соответствующий компонент из панели компонентов в область построения сценария (подробнее см. ["Первый сценарий"](../quick-start/first-scenario.md)).

The workflow nodes are created from 2 types of components :

* Стандартные компоненты - предоставляются в рамках платформы;
* [Производные компоненты](../scenario/derived-component.md) - создаются и настраиваются пользователем. Производный компонент можно создать из комбинации узлов сценария, реализующей произвольную логику обработки.

Таким образом набор средств для реализации различной логики обработки данных не ограничивается стандартными компонентами платформы и может быть расширен самим пользователем.

The [supernode](./control/submodel.md) is most commonly used to create the derived component. The supernode is a special node that can include other workflow nodes. Реализованная в Подмодели логика может быть произвольной, при этом разработчик сценария может рассматривать её как «черный ящик».

The supernode accepts information by means of input ports, performs processing and sends results to output ports. Input and output ports are set by a user.

От обработчика к обработчику могут передаваться как наборы данных - таблицы, так и переменные - объекты, содержащие лишь одно значение. Статистические данные таблиц (например, сумма по столбцу, среднее значение и т.д.) при помощи специального обработчика могут быть преобразованы в переменные.

Переменные, в свою очередь, могут применяться в обработчиках для преобразования таблиц. Поскольку таблицы и переменные имеют разную структуру, то соответствующие им порты не могут быть соединены друг с другом и имеют разное обозначение.

## Стандартные компоненты

### [Трансформация](./transformation/README.md)

Набор компонентов для первоначальной подготовки и простой обработки исходных наборов данных.

* [Группировка](./transformation/grouping.md)
* [Дата и время](./transformation/trans-datatime/README.md)
* [Дополнение данных](./transformation/supplementation.md)
* [Замена](./transformation/substitution/README.md)
* [Калькулятор](./transformation/calc/README.md)
* Калькулятор JS
* [Кросс-таблица](./transformation/cross-table.md)
* [Объединение](./transformation/union.md)
* [Параметры полей](./transformation/fields-parameters.md)
* [Разгруппировка](./transformation/ungrouping.md)
* [Свёртка столбцов](./transformation/rollup-columns.md)
* [Скользящее окно](./transformation/sliding-window.md)
* [Слияние](./transformation/join/README.md)
* [Соединение](./transformation/addition.md)
* [Сортировка](./transformation/sorting.md)
* [Row Filter](./transformation/row-filter/README.md)

### [Управление](./control/README.md)

Компоненты группы предназначены для оптимизации сценариев путем создания подмоделей и повторного использования узлов, а также формирования логики выполнения сценариев при помощи условий и циклов.

* [Выполнение узла](./control/execute-node.md)
* [Подмодель](./control/submodel.md)
* [Узел-ссылка](./control/unit-link.md)
* [Условие](./control/condition.md)
* [Цикл](./control/cycle.md)

### [Исследование](./scrutiny/README.md)

С помощью этих обработчиков можно оценить и/или визуализировать структуру и статистические характеристики данных. Также с их помощью проводятся разведочный и описательный анализы.

* [Автокорреляция](./scrutiny/autocorrelation.md)
* [Корреляционный анализ](./scrutiny/correlation-analysis.md)
* [Факторный анализ](./scrutiny/factor-analysis.md)

### [Предобработка](./preprocessing/README.md)

Предварительная обработка данных для их дальнейшего использования в алгоритмах Data Mining. Применяются такие методы, как заполнение пропусков, сэмплинг, редактирование выбросов и другие.

* [Заполнение пропусков](./preprocessing/filling-omissions.md)
* [Квантование](./preprocessing/quantization.md)
* [Конечные классы](./preprocessing/fine-classes.md)
* [Разбиение на множества](./preprocessing/separating-to-multiplicity.md)
* [Редактирование выбросов](./preprocessing/editing-of-emissions.md)
* [Сглаживание](./preprocessing/smoothing.md)
* [Сэмплинг](./preprocessing/sampling.md)

### [Data Mining](./datamining/README.md)

Обработчики, выделенные в эту группу, являются инструментами для реализации различных методов Data Mining: кластеризация, ассоциативные правила и другие.

* [EM Кластеризация](./datamining/em-clustering.md)
* [Ассоциативные правила](./datamining/associative-rules.md)
* [Кластеризация](./datamining/clustering.md)
* [Кластеризация транзакций](./datamining/clustering-transactions.md)
* [Логистическая регрессия](./datamining/logistic-regression/README.md)
* [Нейросеть (классификация)](./datamining/neural-network-classification.md)
* [Нейросеть (регрессия)](./datamining/neural-network-regression.md)
* [Самоорганизующиеся сети](./datamining/self-organizing-network.md)

### [Переменные](./variables/README.md)

В Loginom имеется возможность создавать и использовать переменные. Обработчики этой группы позволяют проводить различные операции над ними: изменение, создание переменных из таблицы, расчет новых переменных с помощью различных функций.

* [Замена (переменные)](./variables/variables-replace.md)
* [Калькулятор (переменные)](./variables/variables-calc.md)
* [Переменные в таблицу](./variables/variables-to-table.md)
* [Соединение (переменные)](./variables/variables-union.md)
* [Таблица в переменные](./variables/variables-from-table.md)

### [Интеграция](./integration/README.md)

Механизмы интеграции предназначены для обмена данными между платформой Loginom и сторонними внешними системами.

* [SOAP-запрос](./integration/soap-request.md)
* [REST-запрос](./integration/rest-request.md)
* [Выполнение программы](./integration/exec-program.md)
* [Извлечение XML](./integration/extracting-xml.md)