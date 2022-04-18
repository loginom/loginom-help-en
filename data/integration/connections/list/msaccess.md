# ![ ](../../../images/icons/data-sources/db-msaccess_default.svg) MS Access Connection

It is used for connection to the Microsoft Access database.

## Connection Parameters

The following parameters are set during the connection setup:

* **Caption** contains the connection name set by a user.
* **Connection string**: the path to the DB file containing the required data is specified. Parameters can be manually entered, or it is possible to press ![ ](../../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button to call *Open file* window.
* **Test connection**: test of the specified connection settings.
* **Login** is not used for connection to Microsoft Access.
* **Login**: the password set by the DB user is specified.
* **Save password**: when selecting this checkbox, password will be saved in the current connection settings.
* **Show system tables**: when selecting this checkbox in the import wizard that uses this connection, the system DB tables available to a user become visible.
* **Quote names**: if the database objects names (for example, names of tables, fields) contain spaces or reserved characters, it is required to use framing characters fixing the name start and end.
* **Configure quotes** represents the information field that enables to define which framing characters are used for connection to this DB. Square brackets are used for Microsoft Access.
* **Do not use DBMS client**: this parameter is not available for Microsoft Access.
* **Description**: it is possible to provide any reference connection data in this form.

> **Note:** To provide connection to the database, it is required to install Microsoft Office or [Microsoft Access Database Engine](https://www.microsoft.com/en-us/download/details.aspx?id=13255) with the same bitness as the Loginom application/server bitness.

## Compatibility

Versions 95, 97, 2000, 2003, 2007, 2010, 2013 and 2016.

**See also:**

* [Official manufacturer website](https://www.microsoft.com/ru-ru);
* [Product Documentation](https://docs.microsoft.com/ru-ru/).
