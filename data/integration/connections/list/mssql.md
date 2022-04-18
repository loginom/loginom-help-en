# ![ ](../../../images/icons/data-sources/db-mssql_default.svg) MS SQL Connection

It is used for connection to the MS SQL database.

The connection is provided via OLE DB. Either the OLE DB client preinstalled in Windows OS, or SQL Server Native Client is used. It is preferable to use the latter.

The use of [ODBC connection](./odbc.md) is an alternative method of integration with MS SQL.

## Connection Parameters

The following parameters are set during the connection setup:

* **Caption** contains the connection name set by a user.
* **Connection string** is set in a separate window that can be called both by clicking on ![ ](../../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button, and by entering the parameters manually. These settings are used by the OLE DB driver to connect to the required database.
   * The first option with a separate window called when clicking on ![ ](../../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button. The window includes two fields.
      * **Server**: the SQL server host. If it is necessary, the named instance of SQL server is specified using "".
      * **Database**: the name of the database that includes the required data.
   * When the second option based on the manual entering of parameters is used, it is required to provide the colon separated parameters in the string. The following string format is used: `<ServerName>:<Port>:<DatabaseName>`, for example, `host:1433:database1`.
      * **ServerName**: the DBMS server host.
      * **Port**: the TCP port used by DBMS server to provide interaction with the client. If the parameter is null, `1433` is used as the default port.
      * **DatabaseName**: the name of the database that includes the required data.
* **Test connection**: test of the specified connection settings.
* **Login**: login of the DB user. If the login is not specified, the domain authorization is used.
* **Password**: password of the DB user.
* **Save password**: when selecting this checkbox, login and password will be saved in the current connection settings.
* **Show system tables**: when selecting this checkbox in the import wizard that uses this connection, the system DB tables available to a user become visible.
* **Quote names**: if the database objects names (for example, names of tables, fields) contain spaces or reserved characters, it is required to use framing characters fixing the name start and end.
* **Configure quotes** represents the information field that enables to define which framing characters are used for connection to this DB. Square brackets are used for MS SQL.
* **Encoding value** enables to set the message language of the DB server and codepage for the values related to the character types represented not in UNICODE: char, varchar, text.
* **Do not use DBMS client**: this parameter is not available for MS SQL.
* **Clear pool when deactivated** enables to clear the pool of the Loginom Integrator packages frequently used in the batch processing saved for the quick call upon the node deactivation. This parameter is disabled by default.
* **Description**: it is possible to provide any reference connection data in this form.

> **Note:** To provide connection to the database, the clients or ODBC driver must be with the same bitness as the Loginom application/server bitness.

## Compatibility

* Clients.
   * SQL OLE DB.
   * SQL Native Client.

* Servers.
   * SQL Server 2016, 2014, 2012, 2008 R2, 2008, 2005 (including Express edition).
   * SQL Server 2000 (including MSDE).
   * SQL Server 7.
   * SQL Server Compact 4.0, 3.5, 3.1.

> **Important:** The domain authorization process is implemented as user under whose name the Loginom server has been started.

**See also:**

* [Information in the Russian section in Wikipedia](https://ru.wikipedia.org/wiki/Microsoft_SQL_Server);
* [Official manufacturer website](https://www.microsoft.com/ru-ru/sql-server);
* [SQL Syntax Documentation](https://docs.microsoft.com/ru-ru/sql/t-sql/queries/queries).
