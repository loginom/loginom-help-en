# ![Import from the DW](../../images/icons/data-sources/wh-datawarehouse-import_default.svg) Import from Deductor Warehouse

The component is designated for data import from the Data Warehouse [Deductor Warehouse](../../data-format/data-warehouse.md) (hereafter referred to as the Data Warehouse).

> **Important:** For the node operation, it is required to pre-create [Connection](../connections/README.md) to the *Data Warehouse* and connect it with the *Connection* input port.

## Ports

### Input Ports

* ![Port of connections](../../images/icons/app/node/ports/inputs/link_inactive.svg) **Connection** accepts parameters of connection to the Data Warehouse.

### Output Ports

* ![Output port of table](../../images/icons/app/node/ports/inputs/table_inactive.svg) **Data set**: the data imported from the Data Warehouse.

## Wizard

It enables to configure import of the required data from the Data Warehouse.

### Step 1. Select Data Warehouse Object

* **Connection** enables to display a string of connection to data source. It cannot be edited.
* **Activate** provides connection with the Data Warehouse if it has not been established yet. Upon connection establishment, the button is inactive, and the name is changed to *Activated*.
* **Data Warehouse objects** contain a tree list ![Processes](../../images/icons/data-warehouse/fact-tables-folder_default.svg) *Processes* and ![Dimensions](../../images/icons/data-warehouse/dimensions-folder_default.svg) *Dimensions* from which it is required to select only one object, namely,![Process](../../images/icons/data-warehouse/fact-table_default.svg) *Process* or ![Dimension](../../images/icons/data-warehouse/dimension_default.svg) *Dimension*.

### Step 2. Import from Data Warehouse

This page is designated for work with internal items of the object selected at the previous stage: dimensions, attributes and facts.

The wizard window is divided into two areas:

* **Available items** are in the left part. It contains a list of items that can be chosen in accordance with the object selected at the previous stage.
* **Selected items** are in the right part. It contains already chosen items. It enables to specify the required items in the first one and set necessary conditions and values for them.

The item can be only in one list. It is possible to move items between the lists, including drag&drop (*drag&drop*).

### Available Items

* **Parameter**: parameter caption. When cursor hovering, the full caption name appears.
* **Type** enables to display the item type. There are the following items:
   * ![Dimension](../../images/icons/data-warehouse/dimension_default.svg) *Dimension*.
   * ![Fact](../../images/icons/data-warehouse/fact_default.svg) *Fact*.
   * ![Attribute](../../images/icons/data-warehouse/attribute_default.svg) *Attribute*.

It is possible to sort the list by pressing the *Parameter* or the *Type* column. It is possible to select several items by holding down the Shift or Ctrl key.

The context menu:

* ![Move](../../images/icons/toolbar-controls/create-out-column_default.svg) **Move to selected** enables to move the selected item to the *Selected items* list.
* ![Move all](../../images/icons/toolbar-controls/create-out-columns_default.svg) **Move all to selected** enables to transfer all available items to the *Selected items* list.

### Selected Items

* ![Show](../../images/icons/data-warehouse/on_default.svg) **Show** enables to define whether this item will be added in the form of a field to the output data set (if it is disabled, the field will not be added but corresponding filter can be set).
* **Field** is the same as the *Parameter* in the *Available items*.
* **Type** is the same as the *Type* in the *Available items*.
* **Condition** for *Dimensions* and *Attributes* enables to select the filtration condition from the drop-down list.
* **Value** for *Fact* displays the selected [aggregations](../../processors/func/aggregation-functions.md), the filtration value is displayed for other items if a condition is specified.
* ![Delete](../../images/icons/toolbar-controls/delete_default.svg) **Delete** enables to move the required parameter back to the *Available items* list.

> **Note:** if the item showing is disabled, and no *conditions * and/or *values* are specified, upon the list saving, this item will be moved back to the *Available items* list.

If *listed* or *not listed* option is selected in the *Condition* field, it will be possible to edit the list used for comparison in the *Value* field. By pressing ![to be defined](../../images/extjs-theme/form/open-trigger/open-trigger_default.svg) button, the *List of values* window will be opened (refer to the information below).

It is possible to change the order of items.

* ![Move up](../../images/icons/toolbar-controls/moveup_default.svg) **Move up** enables to move the selected item up the list.
* ![Move down](../../images/icons/toolbar-controls/movedown_default.svg) **Move down** enables to move the selected item down the list.

To exclude the item from the list of selected items, it is required to perform the following actions:

* Drag the item from the *Selected items* list to the *Available items* list.
* Press ![Delete](../../images/icons/toolbar-controls/delete_default.svg) *Delete* button.

To clear the whole list, it is required to press ![Delete all](../../images/icons/toolbar-controls/delete-all_default.svg) *Delete all...* button.

The context menu duplicates the general functions:

* ![show](../../images/icons/checkbox-states/checked_default.svg) **Show** enables to define whether this item will be added in the form of a field to the output data set.
* ![Delete](../../images/icons/toolbar-controls/delete_default.svg) **Delete** enables to move the required parameter back to the *Available items* list.
* ![Delete all](../../images/icons/toolbar-controls/delete-all_default.svg) **Delete all** enables to move all parameters back to the *Available items* list.
* ![Move up](../../images/icons/toolbar-controls/moveup_default.svg) **Move up** enables to move the selected item up the list.
* ![Move down](../../images/icons/toolbar-controls/movedown_default.svg) **Move down** enables to move the selected item down the list.

The following hotkeys duplicating some listed commands are available:

* %kbd Delete %: delete.
* %kbd Shift Delete %: delete all.
* %kbd Ctrl Up %: move up.
* %kbd Ctrl Down %: move down.

#### List of Values

It enables to select the rows with which values will be compared.

* ![Get list](../../images/icons/toolbar-controls/get-column-list_default.svg) **Get list** enables to get the list compliant with the selected item.
* ![Check all](../../images/icons/toolbar-controls/check-all_default.svg) **Check all** enables to check all rows.
* ![Uncheck all](../../images/icons/toolbar-controls/uncheck-all_default.svg) **Uncheck all** enables to uncheck all rows.
* ![Invert selection](../../images/icons/toolbar-controls/reverse-check_default.svg) **Invert selection** enables to invert selected and not selected items.
* ![Add](../../images/icons/toolbar-controls/plus_default.svg) **Add** enables to add a new row to the list.
* ![Edit](../../images/icons/toolbar-controls/edit_default.svg) **Edit** enables to edit the row added to the list.

Using the![filter](../../images/icons/toolbar-controls/filter_default.svg) *Filter* field, it is possible to decrease the visible part of the list.

When the work with the list is completed, it is required to press *Apply* button to introduce changes, or *Cancel* button to return to the state before the work with the list.
