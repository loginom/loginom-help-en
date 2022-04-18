# ![wh-oracle](../../../images/icons/data-sources/wh-oracle_default.svg) Connection to Deductor Warehouse [Oracle]

It is used for connection to the [Deductor Warehouse](../../../data-format/data-warehouse.md) Data Warehouse based on Oracle DBMS.

It is possible to provide connection both via DBMS client, and the internal Loginom driver.

## Connection Parameters

The following parameters are set during the connection setup:

* **Caption** contains the connection name set by a user.
* **Connection string**: the string used by the driver for connection to the required database. The string connection format is defined by the used driver (refer to *Do not use DBMS client* parameter below):
   * The string format when DBMS client is used is as follows:
      * **`<ServerName>`** where
         **ServerName**: the DBMS server host as stated in tnsnames.ora configuration file of Oracle server.
   * The string format when the inbox driver is used can relate to the following kind:
      * **`<ServerName>:<Port>:<SID>`** or
      * **`<ServerName>[:<Port>]/<Service_name>`** where:
         * **ServerName**: the DBMS server host.
         * **Port**: the TCP port used by DBMS server to provide interaction with the client.
         * **SID**: the unique name of the DB example (System ID).
         * **ServiceName**: the alias of one or several DB examples.
* **Test connection**: connectivity test with the specified settings.
* **Login**: login of the DB user.
* **Password**: password of the DB user.
* **Parameters**:
   * **Save password**: when selecting this checkbox, login and password will be saved in the current connection settings.
   * **Show system tables**: when selecting this checkbox in the import wizard that uses this connection, the system DB tables available to a user become visible.
   * **Quote names**: if the database objects names (for example, names of tables, fields) contain spaces or reserved characters, it is required to use framing characters fixing the name start and end.
   * **Configure quotes** represents the information field that enables to define which framing characters are used for connection to this DB. Double quotes are used for Oracle.
   * **Do not use DBMS client**: if this option is used, the alternative inbox driver built into the platform is used for connection to DBMS.
   * **Clear pool when deactivated** enables to clear the pool of the Loginom Integrator packages frequently used in the batch processing saved for the quick call upon the node deactivation. This parameter is disabled by default.
* **Description**: it is possible to provide any reference connection data in this field.

> **Note:** If DBMS client is used, it must be with the same bitness as the Loginom application/server bitness.

## Compatibility

Starting from Oracle Database 9i and higher.

> **Important:** UTF16 encoding is used for data exchange with the server.

**See also:**

* [Information on Oracle Database in the Russian section in Wikipedia](https://ru.wikipedia.org/wiki/Oracle_Database);
* [Official website of the Oracle Database manufacturer](https://www.oracle.com/database).
