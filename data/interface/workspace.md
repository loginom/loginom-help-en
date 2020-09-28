# Working Space
Working space consists of a panel of components, toolbar and area of the Workflow construction (refer to Figure 1).

![Working space](./workspace.png)

The panel of components is located on the left. It consists of the following categories:

* Components are represented by a standard library of the Loginom base components.
* [Derived components](../scenario/derived-component.md) are the components created by users according to the base ones.
* [Connections](../integration/connections/README.md) are data sources.

The Workflow construction area is located in the centre. It is an area containing the Worlflow nodes and links between them.

The toolbar that enables the following operations with the construction area and its constituents is located in the upper part:
* ![](../images/icons/toolbar-controls/arrow-rr_default.svg) Show/![](../images/icons/toolbar-controls/arrow-ll_default.svg)Hide component panel enables to open or hide the panel of components.
* ![](../images/icons/toolbar-controls/cursor_default.svg)Object selection mode is a mode used for the Workflow construction by means of standard manipulations.
* ![](../images/icons/toolbar-controls/hand_default.svg)Workflow navigation mode is a mode used for navigation in the Workflow construction area by means of a mouse.
* ![](../images/icons/toolbar-controls/workflow_default.svg) Show as workflow enables to display a Workflow in the standard form (in the form of oriented graph).
* ![](../images/icons/toolbar-controls/table_default.svg)Show as table provides compact display of the Workflow in the form of a table that contains used elements.
* ![](../images/icons/toolbar-controls/v-align-left_default.svg)Vertical alignment provides vertical alignment of the Workflow nodes in the construction area. There are the following types of the vertical alignment:
   * Vertical left alignment
   * Vertical middle alignment
   * Vertical right alignment
   * Vertical upper alignment
   * Vertical center alignment.
   * Vertical bottom alignment
* ![](../images/icons/toolbar-controls/layout_default.svg) Auto node alignment is an automatic placement of nodes in the Workflow area according to their sequence of data processing.
* ![](../images/icons/toolbar-controls/move-front_default.svg)Send selected nodes enables to bring selected nodes and their signatures to:
   * Front
   * Back
* ![](../images/icons/toolbar-controls/order_default.svg) [Customize execution order](../scenario/run-order.md) enables to set one's own order of nodes execution.
* ![](../images/icons/toolbar-controls/run-all_default.svg) Run all enables to run all nodes of the Workflow.
* ![](../images/icons/toolbar-controls/run-current_default.svg) Activate/![](../images/icons/toolbar-controls/stop_default.svg) Deactivate node enables to activate/deactivate a node.
* ![](../images/icons/toolbar-controls/retrain_default.svg) [Retrain node](../scenario/training-processors.md) enables to retrain the selected node.
* ![](../images/icons/toolbar-controls/setup_default.svg) Configure node provides access to setting of the selected node.
* ![](../images/icons/toolbar-controls/batch-mode_default.svg) [Configure node activation mode](../scenario/setting-batch-processing-mode.md) provides configuration of activation mode for the selected node.
* ![](../images/icons/toolbar-controls/clone_default.svg) Clone node enables to clone the selected node.
* ![](../images/icons/toolbar-controls/compose-generic-model_default.svg) Expand/collapse[ supernode](../processors/control/submodel.md) enables to collapse the selected nodes into the Supernode, or expand the selected Supernode into compound nodes.
* ![](../images/icons/toolbar-controls/delete_default.svg) Delete selected enables to delete the selected nodes/links of the Workflow.
* ![](../images/icons/toolbar-controls/derive-node_default.svg)Create derived component enables to create the Derived Component based on the selected node.
* ![](../images/icons/toolbar-controls/show-derived-nodes_default.svg)Show parent nodes for derived shows parent nodes if derived nodes are available.
* ![](../images/icons/toolbar-controls/show-reference-links_default.svg) Show source nodes for [Reference Nodes](../processors/control/unit-link.md) shows the nodes on the basis of which Reference Nodes were created, if any.
* ![](../images/icons/toolbar-controls/preview_default.svg)Show workflow outline enables to open for the navigation purposes a reduced copy of the Workflow construction area suitable for scaling.
* ![](../images/icons/toolbar-controls/info_default.svg)Show/hide property inspector enables to expand/collapse the *Property inspector* window. This button is always located in the far right position on the toolbar.

> **Note:** When the *Property inspector* window is opened, there can be not enough place for some buttons on the toolbar. In this case, ![](../images/icons/toolbar-controls/system-panel-more_default.svg) button with a dropdown list appears on the toolbar. It will contain all other buttons for which there is no enough place on the toolbar.