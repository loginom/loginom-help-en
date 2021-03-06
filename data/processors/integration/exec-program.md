# ![ ](../../images/icons/components/execcmd_default.svg) Выполнение программы

## Описание

С помощью компонента *Выполнение программы* можно запустить на выполнение внешнюю программу (исполняемый файл: cmd, bat, exe и т.д.)

> **Важно:** этот компонент небезопасный, так как предоставляет доступ к программам и файловой системе. Права на эту операцию задаются в [Администрировании](../../admin/parameters.md).

## Порты

### Вход

* ![ ](../../images/icons/app/node/ports/inputs-optional/variable_inactive.svg) — Входные переменные (переменные) — необязательный порт. Имена переменных можно использовать в *Командной строке*, т.е. поддерживается макроподстановка команд: ```%ИмяПеременной%``` — переменная, содержащая команду, которая подается на вход данного узла (см. [Примеры](#primery)).
* ![ ](../../images/icons/app/node/ports/inputs-optional/variable_inactive.svg) — [Управляющие переменные](../../scenario/variables/control-variables.md) (переменные) — необязательный порт. Их можно использовать для задания таких параметров, как *Тайм-аут выполнения узла* и *Завершить программу по тайм-ауту*.

### Выход

* ![ ](../../images/icons/app/node/ports/outputs-optional/variable_inactive.svg) — Исходные переменные и переменные, содержащие информацию об успешности выполнения программы:

   * ![ ](../../images/icons/data-types/integer_default.svg) **Результат выполнения** — переменная целого типа, содержащая значение *0* в случае успешного завершения выполняемой программы;
   * ![ ](../../images/icons/data-types/string_default.svg) **Сообщение об ошибке** — переменная строкового типа, содержащая сообщение об ошибке, если она произошла при выполнении или подготовке к выполнению программы.

## Мастер настройки узла

* **Тайм-аут выполнения узла (мсек.)** — устанавливает время выполнения узла:
   * **0** — узел сразу завершится.
   * **1 и более** — количество миллисекунд, через которые узел перестанет выполняться. Стрелками можно увеличивать или уменьшать тайм-аут с интервалом в 100 миллисекунд.
   * **Бесконечность** — в этом случае узел будет выполняться до тех пор, пока программа не будет закрыта. Для того, чтобы установить время выполнения узла, в значении *Бесконечность* необходимо в поле тайм-аута ввести либо *-1*, либо удалить все цифры.
* **Завершить программу по тайм-ауту** — переключатель позволяет включать/отключать тайм-аут выполнения узла.

> **Важно:** в настройках устанавливается время выполнения узла, а не программы, поэтому если галочка *Завершить программу по тайм-ауту* не установлена, то через определенное тайм-аутом время узел перестанет выполняться, а программа — нет.

## Написание команд

В поле *Текст команды* следует вводить команду следующим образом:

* Если это стандартная программа Windows:
   * ```cmd.exe``` — указывается название программы и ее расширение.
* Если это сторонняя программа:
   * ```C:\Program Files (x86)\Microsoft Office\Office14\EXCEL.EXE``` — указывается абсолютный путь до исполняемого файла.

Для выполнения команд через *cmd.exe* необходимо указывать соответствующие ключи:

* ```/C``` — выполнение указанной команды с последующим завершением;
* ```/K``` — выполнение указанной команды без последующего завершения.

Другие ключи запуска можно посмотреть на соответствующих сайтах по командной строке Windows.

### Текущий каталог проекта

Если проект сохранен, то текущим каталогом для процесса, запускаемого узлом *Выполнение программы*, считается текущий каталог пакета.

> **Примечание:** производный узел, так же, как и любой другой, работает в контексте того пакета, в котором он находится. То есть текущим каталогом для производного узла будет текущий каталог пакета, в котором находится именно производный узел, а не базовый.

#### Desktop-версия Loginom

В Desktop-версии приложения, если проект не сохранен, то текущий каталог совпадает с текущим каталогом Loginom.

#### Серверная версия Loginom

На сервере Loginom, если проект не сохранен, то текущий каталог совпадает с каталогом пользователя.

### Примеры

Пример создания директории через командную строку:

```cmd.exe /C mkdir D:\Dir\```

Пример макроподстановки:

```cmd.exe /C %ИмяПеременной%```

Где ```%ИмяПеременной%``` — переменная, содержащая любую команду для выполнения в командной строке Windows.
