# The First Workflow

In the case of the [Enterprise](https://loginom.ru/platform/pricing#edition-enterprise), [Standard](https://loginom.ru/platform/pricing#edition-standard) and [Team](https://loginom.ru/platform/pricing#edition-team) delivery editions, when starting the software, the home login page is opened. It is required to log in having entered password and login. Login and password are provided by the administrator, but there is a default user - login in the case of the software installation: *user*, without password. There is no authorization for the [Personal](https://loginom.ru/platform/pricing#edition-personal) version.

Upon authorization, the action selection window will be opened (the [Home page](../interface/home-page.md) page). Using this window you can perform the following operations with packages.

* **New package** — creation of the new package. You will be asked to show the path to save the package.
* **New Draft** — creation of the new package without preliminary saving. It is possible to save the package only during the process of work with it.
* **Open Package** — opening of the earlier created package.

> **Important:** The software doesn't auto save. When closing the software window (browser tabs), all changes will be lost.

Upon package selection, a user will enter the working space of the software. It can be divided into four main areas (refer to Figure 1):

1. The main menu with the following buttons is located on the left: Menu, Packages, Navigation, [Files](../location_user_files.md), [Processes](../interface/processes-panel.md).
2. The upper part displays tabs of the opened packages. It contains address line and navigation elements for packages and their parts.
3. Desktop is located to the right of the main menu. It contains the left panel where working components, solution structure (packages and their parts), area of workflow construction and data visualization are displayed.
4. The Processes panel is located in the lower part of the window. It is hidden by default, but it is possibble to lock it.

![Working Space of Studio.](./first-scenario-1.png)

Upon package creation, a user will see the Workflow Construction Area (6) and the Components panel (5) which contains the standard components provided by the platform (refer to Figure 2).

![The Workflow Construction Area and the Components Panel](./first-scenario-2.png)

In the simplest case the workflow will import the data from the external sources, or it will transform them and export (send to report).
Let's create a simple workflow that will form TOP10 list of the best clients.

The workflow will perform the following actions:

* Import of the sales information from the [Sales.txt](../attach/Sales.txt) file.
* Selection of 10 clients with the highest purchase sums.
* Export of the received results.

To use any component in the workflow, it must be dragged from the component panel to the workflow construction area.

Select the [Text file](../integration/import/txt-csv.md) component in the Import section and transfer it to the construction area (refer to Figure 2). In this case, the workflow node responsible for import is created. Icons of possible actions will be displayed after mouse click. Call the [Wizard](../integration/import/txt-csv.md) (refer to Figure 3).

![Call node configuration wizard.](./first-scenario-3.png)

Follow the wizard steps having specified the Sales.txt file location in the File Name parameter.

Execute the node upon its configuration using the menu of possible actions. Now the imported data is present in the output node port. It is possible to view them selecting ![ ](../images/icons/toolbar-controls/show-fast-viewer_default.svg) [Quick View…](../visualization/preview/quick-view.md) in the context port menu (refer to Figure 4).

![Call Quick View](./first-scenario-4.png)

The next algorithm step is calculation of purchase sum for all clients. For this purpose, trasfer the [Grouping](../processors/transformation/grouping.md) component to the working workflow area. The sequence of data processing is set by connection of the output port of the import node with the input grouping port (refer to Figure 5).

![Establish Connection](./first-scenario-5.png)

The Client Card field is set as a group, and the Sum is set as a parameter in the [Grouping](../processors/transformation/grouping.md) Node Wizard. Upon configuration and execution of the grouping node, data about total sums of the clients' purchases are in the output port.

Then this data is sorted in the sum descending order using the [Sorting](../processors/transformation/sorting.md) component. Then this data is transferred to the node used for selection of the first 10 table rows.  For this purpose, the [Row Filter](../processors/transformation/row-filter/README.md) component is used. "№ Row number <= 10" criteria is set in its wizard.

The export node is added to the resulting workflow, and/or the [Visualizer](../visualization/README.md) of results is configured (refer to Figure 6).

![Resulting Workflow](./first-scenario-6.png)

The block of the nodes forming TOP 10 list of clients can be grouped as a separate function by placing them into the [Supernode](../processors/control/submodel.md). For this purpose, it is required to select these nodes and using ![](../images/icons/toolbar-controls/compose-generic-model_default.svg) button create a supernode.

![Selection of the Block of Nodes](./first-scenario-7.png)

![Transformation of the Block of Nodes to the Supernode](./first-scenario-8.png)

Later on, the supernode executing the function set by a user can be published as a derived component and frequently used in other workflows along with standard components. Principles of creation of the solutions based on own components are analysed in the [Design of Workflows](../scenario/README.md) article.

The package must be *saved* before its closure. It can be done in the Package menu (refer to Figure 9).

![Save Package](./first-scenario-9.png)
