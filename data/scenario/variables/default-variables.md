# Предопределенные переменные

## Переменные пакета

Основной кейс использования — [Производные компоненты](../derived-component.md). Переменные предоставляют информацию о Пакете, в котором создан Производный компонент.

Параметры Пакета, в котором создан используемый Производный компонент:

| Имя | Description | Пример |
| :---- | :---- | :---- |
| PackageName | Имя пакета | FunctionLibrary |
| PackageVersion | Версия пакета | 1.0.0 |
| PackageGuid | Идентификатор пакета | {D9AD3962-94A5-4CE0-8909-64D0747B0E9C} |
| PackageFileName | Файл пакета | /user/ProjectName/scripts/FunctionLibrary.lgp |
| PackageFilePath | Путь к файлу пакета | /user/ProjectName/scripts/ |

Параметры Пакета, в котором используется Производный компонент:

| Имя | Description | Пример |
| :---- | :---- | :---- |
| DerivedPackageName | Имя пакета | main |
| DerivedPackageVersion | Версия пакета | 1.0.0 |
| DerivedPackageGuid | Идентификатор пакета | {38A56938-93B6-4981-A5DA-70053DB575EE} |
| DerivedPackageFileName | Файл пакета | /user/ProjectName/scripts/main.lgp |
| DerivedPackageFilePath | Путь к файлу пакета | /user/ProjectName/scripts/ |

## Переменные сессии

| Имя | Description | Пример |
| :---- | :---- | :---- |
| UserName | Логин пользователя, открывший данный Сценарий | user |
| SessionGuid | Идентификатор текущей сессии на сервере Loginom | {AA037666-56F9-4B06-AE6F-AE3E2E00052F} |
