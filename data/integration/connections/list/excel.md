# ![ ](../../../images/icons/data-sources/file-excel_default.svg) MS Excel Connection

It is used for connection to the Microsoft Excel file as to a database.

## Connection Parameters

The following parameters are set during the connection setup:

* **Caption** contains the connection name set by a user.
* **Connection string**: the path to the file containing the required data is specified. Parameters can be manually entered, or it is possible to press ![ ](../../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button to call *Open file* window.
* **Test connection**: test of the specified connection settings.
* **Login** is not used for connection to the Microsoft Excel file.
* **Password** is not used for connection to the Microsoft Excel file.
* **Save password**: when connecting to the Microsoft Excel file, this parameter is not used.
* **Show system tables**: when selecting this checkbox in the import wizard that uses this connection, the system DB tables available to a user become visible.
* **Quote names**: if the database objects names (for example, names of tables, fields) contain spaces or reserved characters, it is required to use framing characters fixing the name start and end.
* **Configure quotes** represents the information field that enables to define which framing characters are used for connection to this DB. Double quotes are used for Microsoft Excel.
* **Do not use DBMS client**: it is not possible to change this parameter for Microsoft Excel.
* **Clear pool when deactivated** enables to clear the pool of the Loginom Integrator packages frequently used in the batch processing saved for the quick call upon the node deactivation. This parameter is disabled by default.
* **Description**: it is possible to provide any reference connection data in this form.

## Compatibility

To connect to the files of Microsoft Excel 2007 and higher (*.xlsx), the system must include the following components matching the Loginom server by bitness:
* Microsoft Excel 2007 and higher;
* [Microsoft Access Database Engine 2016 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=54920).

**See also:**

* [Official manufacturer website](https://www.microsoft.com/ru-ru);
* [Product Documentation](https://docs.microsoft.com/ru-ru/).
