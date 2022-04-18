# ![ ](../../../images/icons/data-sources/db-mysql_default.svg) MySQL Connection

It is used for connection to the MySQL database.

It is possible to provide connection both via DBMS client, and the internal Loginom driver.

## Connection Parameters

The following parameters are set during the connection setup:

* **Caption** contains the connection name set by a user.
* **Connection string** is set in a separate window that can be called both by clicking on ![ ](../../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button, and by entering the parameters manually. These settings are used by the OLE DB driver to connect to the required database.
   * The first option with a separate window called when clicking on ![ ](../../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button. The window includes two fields.
      * **Server**: MySQL server host.
      * **Database**: DB name.
   * When parameters are manually entered, it is required to provide the colon separated parameters in the string. The following string format is used: `<ServerName>:<Port/Shared Memory>:<DatabaseName>`, for example, `localhost:3306:database1`. When Shared-Memory is used, the following way of writing is also possible: `localhost:MYSQL:database1`.
      * **ServerName**: the DBMS server host. The host value must be `localhost` to connect via the Shared Memory protocol.
      * **Port/Shared Memory**: the TCP port used by DBMS server to provide interaction with the client. Or `shared-memory-base-name` option set by the server (it mustn't be the correct port number). If the parameter is null, and *ServerName* is not `localhost`, connection is provided via TCP/IP protocol with default port `3306`.
      * **DatabaseName**: the name of the database that includes the required data. If *Port/Shared Memory* parameter is null, it is allowed to leave this parameter null, in this case all available databases will be shown.
   * When the string is empty, connection to `localhost` is provided in the field.
* **Test connection**: test of the specified connection settings.
* **Login**: login of the DB user.
* **Password**: password of the DB user.
* **Save password**: when selecting this checkbox, login and password will be saved in the current connection settings.
* **Show system tables**: when selecting this checkbox in the import wizard that uses this connection, the system DB tables available to a user become visible.
* **Quote names**: if the database objects names (for example, names of tables, fields) contain spaces or reserved characters, it is required to use framing characters fixing the name start and end.
* **Configure quotes** represents the information field that enables to define which framing characters are used for connection to this DB. Backquotes are used for MySQL.
* **Do not use DBMS client**: if this option is used, the alternative inbox driver built into the platform is used for connection to DBMS.
* **Clear pool when deactivated** enables to clear the pool of the Loginom Integrator packages frequently used in the batch processing saved for the quick call upon the node deactivation. This parameter is disabled by default.
* **Idle-in-transaction timeout**: MySQL server does not control incorrectly disrupted connections. If the client is disabled incorrectly, the server session still exists until timeout is completed. Incomplete transactions lock the DB data. To avoid long-lasting data lock, timeout can be limited by "Idle-in-transaction timeout" parameter. It is set in seconds.
* **Description**: it is possible to provide any reference connection data in this form.

> **Note:** To provide connection to the database via DBMS client, it is required to install the client library files (DLL) with the same bitness as the Loginom application/server bitness.

## Compatibility

* Clients: 5.7, 5.6, 5.5, 5.1, 5.0, 4.1, 4.0 and 3.23
* Servers: 5.7, 5.6, 5.5, 5.1, 4.1 and 4.0

> **Note:** Compatibility with version 8.0 was not tested. It is recommended to use the new authentification method if version 8.0 is used.

**See also**:

* [Information in the Russian section in Wikipedia](https://ru.wikipedia.org/wiki/MySQL);
* [Official manufacturer website](https://www.mysql.com/);
* [SQL Syntax Documentation](https://dev.mysql.com/doc/refman/5.7/en/sql-syntax.html).
