# ![ ](../../../images/icons/data-sources/db-sqlite_default.svg) SQLite Connection

It is used for connection to the SQLite database.

This connection also implements the following features of work with [database import](../../import/database.md).

* Alongside with the standard character collation rules, namely, BINARY, RTRIM and NOCASE, it is possible to use the following ones that are not subject to the SQLite standard.
   * **UNICODE**: the language independent Unicode character collation without case sensitivity.
   * **LOCALIZED**: the language dependent Unicode character collation without case sensitivity. The string comparison result depends on the operational system locale of the Loginom server.
* It is possible to use iLIKE function in the SQL constructions. It implements LIKE feature in the case insensitivity mode of Unicode characters.
* Check by foreign keys is enabled by default.

## Connection Parameters

The following parameters are set during the connection setup:

* **Caption** contains the connection name set by a user.
* **Connection string**: the path to the DB file containing the required data is specified. Parameters can be manually entered, or it is possible to press ![ ](../../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button to call *Open file* window.
* **Test connection**: test of the specified connection settings.
* **Login** is not used for connection to SQLite.
* **Password**: the password set by the DB user is specified for data protection.
* **Save password**: when selecting this checkbox, login and password will be saved in the current connection settings.
* **Show system tables**: when selecting this checkbox in the import wizard that uses this connection, the system DB tables available to a user become visible.
* **Quote names**: if the database objects names (for example, names of tables, fields) contain spaces or reserved characters, it is required to use framing characters fixing the name start and end.
* **Configure quotes** represents the information field that enables to define which framing characters are used for connection to this DB. Double quotes are used for SQLite.
* **Do not use DBMS client**: this parameter is not available for SQLite.
* **Clear pool when deactivated** enables to clear the pool of the Loginom Integrator packages frequently used in the batch processing saved for the quick call upon the node deactivation. This parameter is disabled by default.
* **Encrypted DB**: the checkbox enables to set the DB encryption mode. AES256 encryption is used in this mode, and a password is required.
* **Cache size** enables to set the cache size. The parameter provides the same effect as the DB command does: `"PRAGMA schema.cache_size = pages | -kibibytes;"`. When a positive number is entered, the cache size is specified in pages, and when a negative number is entered, the cache is specified in KiB.
* **Sync mode** enables to set the mode of synchronization with the file system. Selection of this mode affects the DB speed. It increases the speed without synchronization providing the lowest degree of protection against failures and decreasing the speed in order to provide higher degree of protection against failures. The parameter provides the same effect as the DB command does: `"PRAGMA schema.synchronous = 0 | OFF | 1 | NORMAL | 2 | FULL | 3 | EXTRA;"`, and it allows for one of the following options.
   * In the case of *Default*, the FULL mode is used.
   * *Off* (OFF).
   * *Normal* (NORMAL).
   * *Full* (FULL).
   * *Extra* (EXTRA).
* **Transaction journal mode**: the transaction journal mode is set. The parameter provides the same effect as the DB command does: `"PRAGMA schema.journal_mode = DELETE | TRUNCATE | PERSIST | MEMORY | WAL;"`, and it allows for one of the following options.
   * In the case of *Default*, the DELETE (Delete file) mode is used.
   * *Delete* (DELETE).
   * *Truncate* (TRUNCATE).
   * *Persist* (PERSIST).
   * *Memory* (MEMORY).
   * *Write-ahead log* (WAL).
* **Regard NOCASE as UNICODE**: the checkbox redefines collation of NOCASE as UNICODE — the language independent Unicode character collation without case sensitivity.
* **lower, upper for UNICODE**: the checkbox extends the effect of lower, upper functions for all UNICODE characters. If this option is not enabled, lower, upper functions are available only for the Latin letters.
* **LIKE Mode**: it is required to select one of the character collation options to use LIKE function.
   * Case-insensitive ASCII characters.
   * Case-sensitive.
   * Case-insensitive.
* **Create DB if it doesn't exist**: when this checkbox is selected, the database specified in the *Connection string* parameter will be created if it doesn't exist. The new DB is created using UTF-16 encoding.
* **Description**: it is possible to provide any reference connection data in this form.

> **Note:** To provide connection to the database, sqlite3.dll and sqlcipher.dll libraries are used. Their bitness matches the Loginom application/ server bitness. These libraries are included into the Loginom distribution kit. When third-party libraries are used, it is possible to redefine values of *Sync mode* and *Transaction journal mode* parameters by default.

## Compatibility

Versions 3.0 and higher.

**See also:**

* [Information in the Russian section in Wikipedia](https://ru.wikipedia.org/wiki/SQLite);
* [Official manufacturer website](https://sqlite.org);
* [SQL Syntax Documentation](https://sqlite.org/lang.html);
* [PRAGMA Information](https://sqlite.org/pragma.html).
