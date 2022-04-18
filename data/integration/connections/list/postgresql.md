# ![ ](../../../images/icons/data-sources/db-postgres_default.svg) PostgreSQL Connection

It is used for connection to the PostgreSQL database and its operation.

## Connection Parameters

The following parameters are set during the connection setup:

* **Caption** contains the connection name set by a user.
* **Connection string** is set in a separate window that can be called both by clicking on ![ ](../../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button, and by entering the parameters manually. These settings are used by the OLE DB driver to connect to the required database.
   * The first option with a separate window called when clicking on ![ ](../../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button. The window includes two fields.
      * **Server**: the PostgreSQL server host.
      * **Database**: DB name.
   * When parameters are manually entered, it is required to provide the colon separated parameters in the string. The string format is as follows: `<ServerName>:<Port>:<DatabaseName>`, for example, `192.168.0.180:5432:postgres`, where
      * **ServerName**: the DBMS server host.
      * **Port**: the TCP port used by DBMS server to provide interaction with the client.
      * **DatabaseName**: the name of the database that includes the required data.
* **Test connection**: test of the specified connection settings.
* **Login**: login of the DB user. If the login is not specified, the domain authorization is used.
* **Password**: password of the DB user.
* **Save password**: when selecting this checkbox, login and password will be saved in the current connection settings.
* **Show system tables**: when selecting this checkbox in the import wizard that uses this connection, the system DB tables available to a user become visible.
* **Quote names**: if the database objects names (for example, names of tables, fields) contain spaces or reserved characters, it is required to use framing characters fixing the name start and end.
* **Configure quotes** represents the information field that enables to define which framing characters are used for connection to this DB. Double quotes are used for PostgreSQL.
* **Do not use DBMS client** is not available as the inbox driver is always used for PostgreSQL in Loginom.
* **Clear pool when deactivated** enables to clear the pool of the Loginom Integrator packages frequently used in the batch processing saved for the quick call upon the node deactivation. This parameter is disabled by default.
* **Description**: it is possible to provide any reference connection data in this form.

> **Note:** As the inbox driver is used for connection, it is not required to install DBMS client.

## Compatibility

Versions from 8.0 to 10.0.

> **Important:** UTF-8 encoding is used for data exchange with the server.

**See also:**

* [Information in the Russian section in Wikipedia](https://ru.wikipedia.org/wiki/PostgreSQL);
* [Official manufacturer website](https://www.postgresql.org/);
* [SQL Syntax Documentation](https://postgrespro.ru/docs/postgresql);
* [The Russian DBMS (Postgres Pro) based on free open-source DBMS PostgreSQL](https://postgrespro.ru/).
