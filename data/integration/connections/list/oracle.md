# ![ ](../../../images/icons/data-sources/db-oracle_default.svg) Oracle Connection

It is used for connection to the Oracle database.

It is possible to provide connection both via DBMS client, and the internal Loginom driver.

## Connection Parameters

The following parameters are set during the connection setup:

* **Caption** contains the connection name set by a user.
* **Connection string**: the string used by the driver for connection to the required database. The string connection format is defined by the used driver (refer to *Do not use DBMS client* parameter).
   * The string format when the inbox driver is used is as follows: **`<ServerName>:<Port>:<Instance>`**.
      * **ServerName**: the DBMS server host.
      * **Port**: the TCP port used by DBMS server to provide interaction with the client.
      * **Instance**: Oracle Database Instance (SID) that contains the required data.
   * The string format when DBMS client is used is as follows: *`<ServerName>`*.
      * **ServerName**: the DBMS server host as stated in tnsnames.ora configuration file of Oracle server.
* **Test connection**: test of the specified connection settings.
* **Login**: login of the DB user.
* **Password**: password of the DB user.
* **Save password**: when selecting this checkbox, login and password will be saved in the current connection settings.
* **Show system tables**: when selecting this checkbox in the import wizard that uses this connection, the system DB tables available to a user become visible.
* **Quote names**: if the database objects names (for example, names of tables, fields) contain spaces or reserved characters, it is required to use framing characters fixing the name start and end.
* **Configure quotes** represents the information field that enables to define which framing characters are used for connection to this DB. Double quotes are used for Oracle.
* **Do not use DBMS client**: if this option is used, the alternative inbox driver built into the platform is used for connection to DBMS.
* **Clear pool when deactivated** enables to clear the pool of the Loginom Integrator packages frequently used in the batch processing saved for the quick call upon the node deactivation. This parameter is disabled by default.
* **Description**: it is possible to provide any reference connection data in this form.

> **Note:** To provide connection to the database via DBMS client, it is required to install the client library files (DLL) with the same bitness as the Loginom application/server bitness.

## Compatibility

* Clients: 12c, 11g, 10g, 9i, 8i, 8.0
* Servers: 12c, 11g, 10g, 9i, 8i, 8.0, including Oracle Express Edition 11g and 10g

> **Important:** UTF16 encoding is used for data exchange with the server.

**See also:**

* [Information in the Russian section in Wikipedia](https://ru.wikipedia.org/wiki/Oracle_Database);
* [Official manufacturer website](https://www.oracle.com/);
* [Brief SQL Syntax Documentation](http://docs.oracle.com/database/122/SQLQR/toc.htm);
* [Full SQL Syntax Documentation](http://docs.oracle.com/database/122/SQLRF/toc.htm).
