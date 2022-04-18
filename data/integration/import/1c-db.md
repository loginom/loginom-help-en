# ![ ](../../images/icons/data-sources/crm-1cv8-import_default.svg) Import from 1C:Enterprise 8.x

The component is designated for import from 1C database.

> **Important:** For the node operation, it is required to pre-create [connection to 1C:Enterprise 8.x platform](../connections/list/1c.md) and connect it with the *Connection* input port. The connection is performed similar to [connection to DB](../../quick-start/database.md).

## Ports

### Input Ports

* ![ ](../../images/icons/app/node/ports/inputs/link_inactive.svg) Connection accepts parameters of connection to database.
* ![ ](../../images/icons/app/node/ports/inputs-optional/variable_inactive.svg) [Control variables](../../scenario/variables/control-variables.md) (optional port): it is possible to set values of the wizard parameters using variables.

### Output Ports

* ![ ](../../images/icons/app/node/ports/inputs/table_inactive.svg)Imported data set

## Wizard

There are the following parameters in the wizard:

* **Connection** enables to display a string of connection to data source. It cannot be edited.
* **Request text**: the field for request to base entry. It determines structure and content of the imported table.  Both Cyrillic 1C and SQL syntax are supported.

[Preview…](../../visualization/preview/preview.md) button enables to access request accuracy. It displays up to 100 first rows of the resulting table.

## Use of Parameters in Requests

It is possible to use parameters in requests in 1С syntax.

Example 1.

```
SELECT
CurrencyRates.Currency.Code,
CurrencyRates.Currency.Name,
CurrencyRates.Period AS Period,
CurrencyRates.Rate,
CurrencyRates.Multipleness
FROM
RollupLedger.CurrencyRates AS CurrencyRates
WHERE
CurrencyRates.Period BETWEEN &start_date AND &end_date
ORDER BY
DESC period
```

In Example 1 `&start_date` and `&end_date` are constructions of substitution of values of `start_date` and `end_date` input variables of the import node. If these variables are not determined in the input port of the import node, there will be an exception. When using such construction, data type of the transferred variable is considered in the request. It must comply with the data type anticipated by 1C request.

When this substitution construction is used, only simple data types can be passed to the query via variables: logical, string, numeric, date/time.  It is impossible to transfer internal instance 1C variables to the request (for example, objects or references of documents and reference textbooks). When formulating requests, it is required to take it into account.

Example 2.

```sql
SELECT
Period, Nomenclature.Name, Count
FROM
InformationRegister.CalendarNeedsInNomenclature.SliceLast(&Date, Count > &Count) AS Needs
INNER JOIN
Catalog.Nomenclature
ON
Catalog.Nomenclature.Reference = Needs.Nomenclature
WHERE %CONDITION%
```

In Example 2 `%CONDITION%`: the construction of substitution of value of `CONDITION` input variable of the import node. `%CONDITION%` construction in the request text will be replaced with the string value of `CONDITION` variable. If the variable will contain the following value: `Nomenclature.ProductItem = "4561"`, the resulting request will have the following form:

```sql
SELECT
Period, Nomenclature.Name, Count
FROM
InformationRegister.CalendarNeedsInNomenclature.SliceLast(&Date, Count > &Count) AS Needs
INNER JOIN
Catalog.Nomenclature
ON
Catalog.Nomenclature.Reference = Needs.Nomenclature
WHERE Nomenclature.ProductItem = "4561"
```

Such substitution construction enables to formulate the request text in a dynamic manner in the course of the workflow execution.
