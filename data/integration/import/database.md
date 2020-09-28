# ![ ](../../images/icons/data-sources/db-database-import_default.svg) Import from Database

The component is designated for data set import from DBMS. The node created on the basis of this component enables to import a table or view from database, or results of execution of the [SQL](https://wiki.loginom.ru/articles/sql.html) query set by a user.

It is allowed to use [Control variables](../../scenario/variables/control-variables.md) in the SQL query text as parameters and macro substitution. It allows for dynamic generation of the request sent to the server. 

> **Important:** For the node operation, it is required to pre-create [connection](../connections/README.md) to database and connect it with the *Connection* input port. [Example of the DB connection and operation](../../quick-start/database.md).

## Ports

### Input Ports

* ![ ](../../images/icons/app/node/ports/inputs/link_inactive.svg) **Connection** accepts parameters of connection to database.
* ![ ](../../images/icons/app/node/ports/inputs-optional/variable_inactive.svg) **Control variables** (optional port): it is possible to set values of wizard parameters using variables.

### Output Ports

* ![ ](../../images/icons/app/node/ports/inputs/table_inactive.svg) **Data set** is a table with imported data.

## Wizard

There are the following parameters in the wizard:

* **Connection** enables to display a string of connection to data source. It cannot be edited.
* **List *Tables/Views***. The data source tables and views available for import are selected from the list. To display the list, connection must be activated by means of the *Activate* button.
* ![ ](../../images/extjs-theme/splitter/mini-left.svg) / ![ ](../../images/extjs-theme/splitter/mini-right.svg) — hides/shows the *Tables/Views* list.
* **Area of selection of variant of data retrieval from DB** contains two tabs:
   * **Table/View** enables to retrieve set fields of the DB object. For this purpose, it is required to mark fields of the DB object in the *Table/View* list that was selected in the *Tables/Views* list.
   * The **SQL query** enables to form the resulting data set by means of the SQL query. For this purpose, it is required to enter text of the database query in the *SQL query* tab. When finalizing the SQL query text, it is possible to use values of the input port variables that enables to improve processing of queries and provide flexible database use.

The [Preview…](../../visualization/preview/preview.md) button enables to access request accuracy. It displays up to 100 first lines of the resulting table.

## Use of Variables in Queries

Variables can be used in the SQL queries in the following ways:

* As **parameter**: a defined value is set for the variable. The parameter is written with a colon in the query text, for example: `:var1`. The variable type will be taken into account in this case, for example, the string will be in quotation marks.  It is allowed to use parameters only in the *WHERE* section.
* As **macro substitution**: the SQL query or its any part is specified as the variable. It must be marked with percent signs in the query text, for example, `%condition%`.

> **Note:** if the substitution construction is in quotation marks, quotation marks are prioritized but not the substitution.

%spoiler%Example:%spoiler%

```sql
SELECT * FROM %tables%
WHERE
   %cond1% :TitlePart
   AND Books.year > :MinYear
   AND Publisher.Name LIKE '%Media%'
```

where 

| variable name | type | example value |
|:---|:---|:---|
| tables | string | Books JOIN Publisher ON Books.PubId = Pub.Id |
| cond1 | string | title LIKE |
| TitlePart | string | Adventures% |
| MinYear | integer | 2005 |
| Media | string | Astra Info |

In this case, `'%Media%'` is not a macro substitution, that's why no replacement with the variable value will take place.

Consequently, the following query will be generated:

```sql
SELECT * FROM Books JOIN Publisher ON Books.PubId = Pub.Id
WHERE
   title LIKE 'Adventures%'
   AND Books.year > 2005
   AND Publisher.Name LIKE '%Media%'
```

%/spoiler%
