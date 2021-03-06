# ![ ](../../images/icons/data-sources/file-excel-import_default.svg) Импорт из Excel-файла

Используется для импорта данных из файлов Microsoft Excel.

### Входные порты

* ![ ](../../images/icons/app/node/ports/inputs-optional/variable_inactive.svg) [Управляющие переменные](../../scenario/variables/control-variables.md) (необязательный порт) — переменными можно задать значения параметров мастера настройки.

### Выходные порты

* ![ ](../../images/icons/app/node/ports/inputs/table_inactive.svg) Импортированная таблица.

## Мастер настройки

Мастер содержит несколько этапов настройки.

### Шаг 1. Импорт из Excel файла

На первом этапе настройки указываются следующие параметры:

* **Хранилище файлов** — выводит информацию о способе подключения к файлу-источнику.
* **Имя файла** — задает путь к импортируемому файлу при локальном подключении, либо имя файла при использовании подключения к папке. Кнопка ![ ](../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) вызывает диалог выбора файла.
* Группа параметров *Область данных*.
   * **Выбор объекта** — предлагается выбрать один из вариантов выбора объекта Excel, содержащего импортируемые данные.
      * **По номеру** — по порядковому номеру листа книги.
      * **По имени** — по наименованию листа книги.
      * **Именованный диапазон** — по наименованию созданного в книге именованного диапазона.
   * **Весь лист** — область листа, содержащего данные для импорта, определяется автоматически.
   * **Стиль ссылок** — предлагается выбрать один из вариантов обозначения ячеек листа Excel.
      * **A1** — в формате, в котором строка ячейки обозначается латинскими буквами, а столбец — цифрами.
      * **R1C1** — в формате R[x]C[y], где x — номер строки ячейки, y — номер столбца ячейки.
   * **Диапазон** — диапазон импортируемых ячеек, заданных в формате `[адрес верхней левой ячейки]:[адрес правой нижней ячейки]`.
   * **До последней строки** — при выборе этой опции диапазон ячеек, заданный в параметре *Диапазон*, будет расширен до последней строки.
* **Пустые строки** — поскольку диапазон ячеек, заданный предыдущими параметрами, может содержать пустые строки, то предлагается выбрать один из вариантов их обработки.
   * **Импортировать** — пустые строки будут импортированы.
   * **Исключить** — пустые строки не будут импортированы.
   * **До первой пустой строки** — строки будут импортированы до первой пустой строки.
* **Количество строк заголовка** — количество верхних строк заданного предыдущими параметрами диапазона, которые не будут импортированы.

Табличная часть мастера предназначена для отображения исходных данных и диапазона импортируемых ячеек. Значение параметра *Диапазон* можно задать при помощи выделения мышью ячеек таблицы.

### Шаг 2. Настройка полей

На этапе настройки указываются следующие параметры:

* Отобразить:
   * **Результат** — в табличной части окна мастера будет показан результат преобразования данных с учетом установленных параметров полей.
   * **Исходные данные** — в табличной части окна мастера будет показан исходный вариант загружаемых данных.

Табличная часть окна мастера предназначена для настройки параметров импорта для каждого поля набора данных.

* **Кол-во строк для анализа** — задает количество строк данных, которые будут представлены в таблице для анализа (от 1 до 200);
* ![Обновить все](../../images/icons/toolbar-controls/refresh_default.svg) **Обновить все** — перечитывает указанное количество строк в таблицу и производит автоматическое формирование результирующего набора данных;
* ![Обновить данные](../../images/icons/toolbar-controls/refresh-data_default.svg) **Обновить данные** — только перечитывает указанное количество строк в таблицу.

Следующие настройки применяются для формирования результирующего набора данных вручную:

* **Имя** — задается уникальное имя поля.
* **Метка** — задает пользовательское описание поля.
* **Тип данных** — [тип данных](../../data/datatype.md) , в который будет преобразовано текстовое значение поля.
* **Вид данных** — [вид данных](../../data/datakind.md), задается списком значений:
   * Неопределенный.
   * Непрерывный.
   * Дискретный.
* **Использовать** — флаг включения поля в результирующий набор данных.
