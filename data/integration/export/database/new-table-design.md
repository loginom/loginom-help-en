# Create New Table

This window has two tabs:
* Configure
* SQL query

%spoiler%Example of filling in:%spoiler%

{% tabs one="Configure", two="SQL query" %}

{% content "one" %}
![Configure fields of the new table](./new-table-design-1.png)

{% content "two" %}
![Representation of the created table in the form of SQL query](./new-table-design-2.png)

{% endtabs %}

%/spoiler%

## Configure

The following data is set below:
* Table name is a unique table name in DB.
* Table fields specifying the following parameters:
   * Field name in the [permissible format](../../../data/datasetfieldoptions.md).
   * Type of the field data.
   * Size (only for the string field): the maximum string length; by default, it is equal to 50. It is required to adjust the parameter value set by default according to the exported data, if relevant.

> **Important:** When exceeding the maximum value of the exported string length, the export error will occur.

The following buttons are used to edit the list of fields :
* ![](../../../images/icons/toolbar-controls/moveup_default.svg)/![](../../../images/icons/toolbar-controls/movedown_default.svg) moves the selected field defining its position in the list of fields of the created table;
* ![](../../../images/icons/toolbar-controls/plus_default.svg) adds a new field to the table;
* ![](../../../images/icons/toolbar-controls/autosync_default.svg) sets the list and features of fields as in the table connected to the input port of the handler;
* ![](../../../images/icons/toolbar-controls/delete-all_default.svg) deletes all fields in the new table.

## SQL Query

This tab enables to view the SQL query type defining the table structure. <br>