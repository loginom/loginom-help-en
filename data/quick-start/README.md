# Start Operation

To solve the analysis tasks, [**Loginom**](https://loginom.ru) allows for data import from different sources and application of the required processing algorithms. It is possible to view results in the system or to export them to the external data receivers.

Thus, the platform can be used both for creation of indepenent analytical solutions, and for development of modules integrated with external systems.

One of the main concepts on which the [**Loginom**](https://loginom.ru) platform is based is the [Workflow](./first-scenario.md).

The **Workflow** is a sequence of actions that must be performed for data analysis. It is a combination of data processing nodes configured by a user to solve particular tasks.

The workflow node performs a separate operation with data. A list of possible operations is represented by a number of ready *components*.

The processing sequence is determined by connection of the previous workflow node output and input of the subsequent one. The handler input and output are *input* and *output [ports](../scenario/ports/README.md)*.

![Workflow example](./readme-1.png)

The workflow nodes are created from 2 types of components :

* **Standard components** are provided by the platform.
* **Derived components** are created and configured by a user.

The derived components can be created from combination of the workflow nodes implementing the random processing logics.

Thus, a set of tools for implementation of different data processing logics is not limited by standard platform components, and it can be expanded by users.

The [supernode](../processors/control/submodel.md) is most commonly used to create the derived component.

The supernode is a special node that can include other workflow nodes. Random logics can be implemented in the supernode. At the same time, the workflow handler can consider it as the "[black box](https://wiki.loginom.ru/articles/black-box.html)". The supernode accepts information by means of input ports, performs processing and sends results to output ports. Input and output ports are set by a user.

The "Workflow Example" figure shows the ["ABC analysis"](https://wiki.loginom.ru/articles/abc-analysis.html) node that is a derived component - supernode.

!["ABC Analysis" Supernode Nodes](./readme-2.png)

The supernode can also include other supernodes. Nesting of supernodes inside each other is not limited.

Types of ports of the workflow nodes:

<table>
    <tr>
        <th align="left" width="150">Port</th>
        <th align="left">Description</th>
    </tr>
    <tr>
        <td><img src="../images/icons/app/node/ports/inputs/table_inactive.svg"> Table</td>
        <td>It is a structured set of data that are organised in the form of two-dimensional structure consisting of columns and rows. Cells of such table contain the data elements: rows, numbers, dates, logical values.</td>
    </tr>
    <tr>
        <td><img src="../images/icons/app/node/ports/inputs/variable_inactive.svg"> Variables</td>
        <td>They are objects containing only one value. It is possible to transform the data from tables to variables and vice versa using the special handlers.</td>
    </tr>
     <tr>
        <td><img src="../images/icons/app/node/ports/inputs/tree_inactive.svg"> Data tree</td>
        <td>It is a set of data in the form of hierarchic tree-like structure.</td>
    </tr>
    <tr>
        <td><img src="../images/icons/app/node/ports/inputs/link_inactive.svg"> Connections</td>
        <td>They define configuration for work with external sources and data receivers.</td>
    </tr>
</table>

As tables, variables and connections have different structure, the ports corresponding to them cannot be connected with each other, and they are differently identified.

Number of the node inputs and outputs varies according to functionality. The node inputs can be automatically (when providing a link) or manually configured.
