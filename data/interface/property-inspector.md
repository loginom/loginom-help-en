# Property Inspector
*Property inspector* is intended for receipt of information on the workflow node properties.

The *Property inspector* window is located in the right part of the screen on the *Workflow* and *Connections* pages. It is collapsed by default.

To view the node properties, it is required to select it and press ![Show/hide property inspector](../images/icons/toolbar-controls/info_default.svg) button on the toolbar.

> **Note:** ![Show/hide property inspector](../images/icons/toolbar-controls/info_default.svg) button is always located in the far right position on the toolbar.

It is possible to open the *Property inspector* window using the context menu of the workflow construction area by ticking ![](../images/icons/toolbar-controls/info_default.svg) **Show/hide property inspector** (tick the box).

The workflow fragment with the opened *Property inspector* window is shown on figure below for the *Calculator* node:

![Property inspector](./scenario-property-inspector.png)

The node properties (caption of properties) are displayed in the form of a tree.

The tree root in the *Property inspector* contains the component name used as a basis for the workflow node creation. The node caption is displayed in the *Value* column. The root tree node is always expanded. It is not possible to collapse it.

> **Note:** It is not possible to change the order of the *Properties* and *Value* columns.

It is possible to sort nodes in the *Property inspector* tree. For this purpose, it is required to click the header of the *Property* column. Subsequent pressing the header enables to change the sorting order or cancels it.

It is possible to select with mouse cursor any cell or range of cells of the *Property inspector* by clicking and copy its (their) value by pressing *Ctrl+C* combination of keys.

Screen tips are used for the cells in which there is no enough place for text.

The *Property inspector* context menu contains the following commands:

* ![](../images/icons/toolbar-controls/open-all_default.svg) **Expand** enables to expand the tree node.

* ![](../images/icons/toolbar-controls/collapce-all_default.svg) **Collapse** enables to collapse the tree node.

The context menu commands enable to collapse/expand all nodes in the properties tree simultaneously. For this purpose, it is required to select the root node and call corresponding command of the context menu.

When changing the node settings, the *Property inspector* updates the properties tree.

> **Important:** If the node is locked (node execution is in progress or node configuration wizard is opened), it is not possible to view its properties. The following message will be displayed in the *Property inspector* for such node: "Node is locked, try later".

If no node was selected, or several nodes were selected, the following invitation will be in the *Property inspector*: "Select a node to view its properties".




