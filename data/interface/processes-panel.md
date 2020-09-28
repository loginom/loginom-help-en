# "Processes" Panel

"Processes" panel enables to receive additional information on the data processing processes by the Workflow nodes during the current Loginom session. Processes and nodes/subnodes which are performed in them are hierarchically fixed on the panel. Sequence numbers were assigned to them. Each new process starts from the "Nodes activation" string. It is explained by the fact that several nodes at once can be run simultaneously at the Workflow start (refer to Figure 1).

!["Processes" panel](./information-panel-1.png)

The panel has the following structure:

* # — sequence number.
* Process — processes (names) and their constituents are hierarchically specified. When pressing the process name, the node required for its execution will be found and selected in the Workflow.
* **%** — percentage of the process execution.
* Processing:
   * ![](./information-panel-2.png) — processing process is in progress, and it is not possible to calculate its termination time in advance.
   * ![](./information-panel-3.png) — execution progress of the current process as data are processed.
   * ![](./information-panel-4.png) — successful completion (processing is completed).
   * ![](./information-panel-5.png) — information on the process execution results has not been received yet.
   * ![](./information-panel-6.png) — an error occurred while the process execution (processing is not completed).
   * ![](./information-panel-7.png) — the process execution has not started yet, an error occurred.
* ![](../images/icons/toolbar-controls/stop-all_default.svg) — to stop all processes.
   * ![](../images/icons/toolbar-controls/stop_default.svg) — to stop a given process.
* ![](../images/icons/toolbar-controls/delete-all_default.svg) — to delete all finished processes.
   * ![](../images/icons/toolbar-controls/delete_default.svg) — to delete a given process from the list.
* Error — error text is specified, should it occur. Full error text will be displayed, when this text pressing.
* Start — date and time of the process start.
* End - date and time of the process end.
* Processing time — difference between start and end of the processing process.

Selecting the process on the information panel, it is possible to call the context menu containing the following actions:

* ![](../images/icons/toolbar-controls/stop-all_default.svg) **Cancel** enables to cancel execution of the selected process.
* ![](../images/icons/toolbar-controls/stop_default.svg) **Cancel all processes...** enables to cancel execution of all processes.
* ![](../images/icons/toolbar-controls/delete_default.svg) **Remove from list** enables to remove the process from the information panel list.
* ![](../images/icons/toolbar-controls/delete-all_default.svg) **Delete all completed processes...** enables to delete all completed processes from the information panel list.
* **Show node** enables to show the selected node in the Workflow construction area.
* **Show details** enables to display an error message delivered by a node.
* **Show completed processes** enables to change display of the processes on the panel:
   * If ![](../images/icons/toolbar-controls/apply_default.svg) is available, it shows all processes, with the exception of those processes that have been removed by a user.
   * If ![](../images/icons/toolbar-controls/apply_default.svg) is not available, it shows only active processes and the processes in which errors occurred. If none of the processes is executed at the moment, and there were no errors in the completed processes, there will be no data on the information panel.

The information panel is hidden by default. It can be opened by pressing ![](../images/icons/systempanel_status/systempanel_status_default-01.svg) button located in the left low corner. To keep the information panel opened when working with the Workflow, it must be locked by pressing ![](../images/icons/toolbar-controls/unpin_default.svg) button. Pressing ![](../images/icons/toolbar-controls/pin_default.svg) will unlock the panel.
![](../images/icons/toolbar-controls/clear_default.svg) button will close the panel.
