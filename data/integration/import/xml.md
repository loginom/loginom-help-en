# ![ ](../../images/icons/data-sources/file-xml-import_default.svg) Import from the XML File

The component is designated for data tables import from the XML files.

> **Important:** For the node operation, it is required to pre-create [connection to the XSD schema](../connections/list/schemes.md) and connect it with the *Connection* input port. The connection is performed similar to [connection to DB](../../quick-start/database.md).

## Ports

### Input

* ![ ](../../images/icons/app/node/ports/inputs-optional/variable_inactive.svg) [Control variables](../../scenario/variables/control-variables.md) (optional port): it is possible to set values of the wizard parameters using variables.
* ![ ](../../images/icons/app/node/ports/inputs/link_inactive.svg) Connect to XSD schema source (required port) allows for connection to the *Connection to set of the XSD schemas* configured earlier.

### Output

* ![ ](../../images/icons/app/node/ports/inputs/table_inactive.svg) Data set - imported data set.

## Wizard

### Step 1. Import from XML File

* **File storage** enables to display information on method of connection to the source file.
* **File name** enables to set a path to the imported file when the connection is local, or a file name when using connection to a folder. ![ ](../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button calls the file selection dialog.
* **Preview selected file** enables to view content of the file selected for import.

### Step 2. Imported Fields

* **Connection**: the state of connection to the XSD schema.
* **Root element**: selection of the XSD schema root element according to which data will be imported. The area displaying the hierarchic structure of the selected root element is located below. It is required to place the checkboxes for the elements that form the fields of the imported table.
* **Default time zone**: the *Date/Time* type values are transformed when extracting from XML according to the following algorithm:
   * If the time zone is specified for the value, it is transformed to the current time zone of the Loginom server.
   * If the time zone is not specified for the value, the following conditions are met:
      * If *Default time zone* is specified, the value is transformed to the current time zone of the Loginom server based on the assumption that it has the time zone specified in the *Default time zone* parameter.
      * If *Default time zone* is not specified, the value is not changed.
* **Repeat single values**: if there are a single item and nested sequence included into a sequence, the single item values will be repeated for each row formed from the nested sequence.
* **Check for strict XSD validation**: when this checkbox is selected, XML is validated for strict compliance with the XSD schema. Otherwise, the check is performed in the simplified accelerated mode. The simplified check procedure is performed faster, however, it does not secure correct data extraction from XML if there are undetected validation errors.
* **Generate composite field captions**: if this checkbox has been selected, hierarchy relative to the root element will be displayed in each field caption. For example, complex `ROOT|PERSON|ACCES-LEVEL` caption will be generated for the imported table field that contains the data of `ACCESS-LEVEL` attribute of `PERSON` element from the root element of `ROOT` file. When this checkbox is not available, the field will get `ACCESS-LEVEL` name.
