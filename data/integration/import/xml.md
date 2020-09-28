# ![ ](../../images/icons/data-sources/file-xml-import_default.svg) Import from the XML File

The component is designated for data tables import from the XML files.

> **Important:** For the node operation, it is required to pre-create [connection to the XSD schema](../connections/list/schemes.md) and connect it with the *Connection* input port. The connection is performed similar to [connection to DB](../../quick-start/database.md).

## Ports

### Input

* ![ ](../../images/icons/app/node/ports/inputs-optional/variable_inactive.svg) [Control variables](../../scenario/variables/control-variables.md) (optional port): it is possible to set values of wizard parameters using variables.
* ![ ](../../images/icons/app/node/ports/inputs/link_inactive.svg) Connection to the XSD schema source (optional port) enables connection to the *Connection to set of the XSD schemas* configured earlier.

### Output

* ![ ](../../images/icons/app/node/ports/inputs/table_inactive.svg) Data set - imported table.

## Wizard

### Step 1. Configuration of Connection to the XML File

* **File storage** enables to display information on method of connection to the source file.
* **File name** enables to set a path to the imported file when the connection is local, or a file name when using connection to a folder. ![ ](../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button calls the file selection dialog.
* **Preview selected file** enables to view content of the file selected for import.

### Step 2. Imported Fields

* **Connection** is a state of connection to the XSD schema.
* **Root element** means selection of the XSD schema root element according to which data will be imported. The area displaying the hierarchical structure of the selected root element is located below. It is required to place the flags for the elements that form the fields of the imported table.
* **Default time zone**: the *Date/time* type values are transformed when extracting from XML according to the following algorithm:
   * If the time zone is specified for the value, it is transformed to the current time zone of the Loginom server.
   * If the time zone is not specified for the value, the following conditions are met:
      * If *Default time zone* is specified, the value is transformed to the current time zone of the Loginom server based on the assumption that it has the time zone specified in the *Default time zone* parameter.
      * If *Default time zone* is not specified, the value is not changed.
* **Repeat single values**: if there are a single item and nested sequence included into a sequence, the single item values will be repeated for each row formed from the nested sequence.
* **Check for strict XSD validation**: when flag placing, XML is validated for strict compliance with the XSD schema. Otherwise, the check is performed in the simplified accelerated mode. The simplified check procedure is performed faster, however, it does not secure correct data extraction from XML if there are undetected validation errors.
* **Generate composite field captions**: if this flag has been placed, hierarchy relative to the root element will be displayed in each field caption. For example, complex `ROOT|PERSON|ACCES-LEVEL` caption will be generated for the imported table field that contains data of the `ACCESS-LEVEL` attribute of the `PERSON` element from the root element of the `ROOT` file. When this flag is absent, the field will get the `ACCESS-LEVEL` name.
