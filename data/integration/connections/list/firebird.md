# ![ ](../../../images/icons/data-sources/db-firebird_default.svg) Firebird Connection

It is used for connection to the Firebird database and its operation.

## Connection Parameters

The following parameters are set during the connection setup:

* **Caption** contains the connection name set by a user.
* **Connection string** is set in a separate window that can be called by clicking on ![ ](../../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button. Two connection types are supported.
   * **Local**: connection without the use of the Firebird server; only a path to the DB is specified.
   * **Remote**: connection with the use of the Firebird server.
      * **Server**: the Firebird server host.
      * **Protocol**: the protocol that is used by the server for interaction with a client.
* **Test connection**: test of the specified connection settings.
* **Login**: login of the DB user. If the login is not specified, the domain authorization is used.
* **Password**: password of the DB user.
* **Save password**: when selecting this checkbox, login and password will be saved in the current connection settings.
* **Show system tables**: when selecting this checkbox in the import wizard that uses this connection, the system DB tables available to a user become visible.
* **Quote names**: if the database objects names (for example, names of tables, fields) contain spaces or reserved characters, it is required to use framing characters fixing the name start and end.
* **Configure quotes** represents the information field that enables to define which framing characters are used for connection to this DB. Double quotes are used for Firebird.
* **Encoding value** provides encoding of characters according to which the server data will be interpreted.
* **Do not use DBMS client**: it is not possible to change this parameter for Firebird.
* **Clear pool when deactivated** enables to clear the pool of the Loginom Integrator packages frequently used in the batch processing saved for the quick call upon the node deactivation. This parameter is disabled by default.
* **Description**: it is possible to provide any reference connection data in this form.

> **Note:** To provide connection to the database, it is required to install the client library files (DLL) with the same bitness as the Loginom application/server bitness.

In the case of the multiple user access to the DB, it is recommended to use the Firebird server to avoid access lock.

> **Important:** The domain authorization process is implemented as user under whose name the Loginom server has been started.

## Compatibility

Starting from Firebird 2.5 and higher.

**See also:**

* [Information in the Russian section in Wikipedia](https://ru.wikipedia.org/wiki/Firebird);
* [Official developer website](https://firebirdsql.org/);
* [SQL Syntax Documentation](https://www.firebirdsql.org/file/documentation/reference_manuals/fblangref25-en/html/fblangref25-dml.html).
