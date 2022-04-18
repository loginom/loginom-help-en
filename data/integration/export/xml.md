# ![ ](../../images/icons/data-sources/file-xml-export_default.svg) Export to the XML File

The component is designated for the data tables export to the XML files.

> **Important:** For the node operation, it is required to pre-create [connection to the XSD schema](../connections/list/schemes.md) and connect it with the *Connection* input port. The connection is performed similar to [connection to DB](../../quick-start/database.md).

## Ports

### Input

* ![ ](../../images/icons/app/node/ports/inputs/table_inactive.svg)Data source: the data table to be exported.
* ![ ](../../images/icons/app/node/ports/inputs-optional/variable_inactive.svg) [Control variables](../../scenario/variables/control-variables.md) (optional port): it is possible to set values of the wizard parameters using variables.
* ![ ](../../images/icons/app/node/ports/inputs/link_inactive.svg) Connect to XSD schema source (required port) allows for connection to the *Connection to set of the XSD schemas* configured earlier.

## Wizard

### Step 1. Configuration of the Export File

* **File storage** enables to display information on method of connection to the destination file.
* **File name** enables to set a path to the destination file when the connection is local, or a file name when using connection to a folder. ![ ](../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button calls the file selection dialog.
* **Configure Formatting**: this area includes the following checkboxes.
   * **Write Byte Order Mark** enables to write [marker of bytes sequence](https://ru.wikipedia.org/wiki/Маркер_последовательности_байтов).
   * **Add indents and line breaks**: each line will correspond to one item before which tab stop will be placed in the export file.
   * **Escape tabs and line breaks in attributes**: replacement of tab characters in attributes of the output file to *`&#x9;`* and line feed character to *`&#xA;`*
   * **Escape single and double quotes**: replacement of single quotes in the output file to *`&apos;`* and double quotes to *`&quot;`*.

### Step 2. Fields Mapping for Export

* **Connection**: the state of connection to the XSD schema.
* **Root element**: selection of the XSD schema root element according to which data will be exported.
* **Object linking**: the list of the exported table fields and hierarchic XML structure that are required to map to each other. Types of the table field data and linked object must coincide. It is possible to auto link the lists using ![ ](../../images/icons/toolbar-controls/auto-connect_default.svg) *Auto link all* button. If the link between the field and object has been incorrectly established, it can be deleted by pressing ![ ](../../images/icons/link-grid/remove-link_hover.svg) button in the line. If it is necessary, it is required to use ![ ](../../images/icons/toolbar-controls/remove-all-links_default.svg) *Delete all links* button to delete all links. The table fields that are mapped to any item are marked in bold text. Apart from the automatic mode, it is possible to link fields and XML objects manually in two ways.
   * **Drag-and-drop method**: drag the field caption to the item.
   * It is required to select the item to be linked, and left-click on its cell in the *Related fields* column. The window for selection of the fields suitable for linking will be opened. Switch button in the state of ![ ](../../images/icons/filter-switcher/filterswitch-on_default.svg) filter displays in the selection window only the fields that are not linked to any items yet, and in the common ![ ](../../images/icons/filter-switcher/filterswitch-off_default.svg) state it displays all fields for selection.
* **Specify time zone**: specification of the time zone for the computer used for export for the date/time data format.
   * Do not specify.
   * Do not specify for Date: do not specify the time zone for the Date type items.
   * Specify always.
