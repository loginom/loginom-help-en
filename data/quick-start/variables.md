# Variables Use

Alongside with the data sets constituting data table, the object used in calculations can be a variable in Studio.

**Variable** is a named value of one of the possible [data types](../data/datatype.md).

The variables port is designated for receipt and transfer of variables from node to node. Such port can accept several variables as input data or deliver them as output data.

Thus, a list of variables can be transferred from node to node.

Examples of the variables use:

* The variable in the formula providing calculation of the expression value using the [Calculator](../processors/transformation/calc/README.md).
* The variable as the parameter of the [Condition](../processors/control/condition.md) component.

## Control Variables

Variables can be also used to set parameters of the node settings.

Thus, the node settings can be the calculation subject matter in the course of the workflow execution. It allows for more flexible implementation of the data processing logics.

Examples of the control variables use:

* The variable can be also used as the criteria parameter of the [Row Filter](../processors/transformation/row-filter/README.md) component.
* The variable as the SQL query parameter in the case of [Import from database](../integration/import/database.md), the variable contains the SQL query text.