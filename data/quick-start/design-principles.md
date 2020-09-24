# Design Principles

The **Project** is a complex of workflows, files, data sources and other elements designated for solution of a particular analytical task.

The project can include several packages due to the fact that each package can provide its objects to other packages using the link mechanism.

## Structural Approach

The project construction is based on the *structural design* methodology— representation of an algorithm in the form of hierarchical structure of blocks.

Each block can be represented on its hierarchical level in the form of the "black box" performing its independent subtask. It is possible to change the subtask solution mechanism inside the "black box". But on the whole, the project is still operable and wil perform the set tasks.

The project designed in such a way has a clear and transparent structure. It allows for development and support of complex projects. It also helps to delegate solution of the selected subtasks.

The "top-down" design (from the general assignment of a task to separate subtasks) is typical of such approach. Solution of the set task is described at the first design step specifying independent subtasks. Subtasks are similarly described at the next step with specification of the next level elements.

Thus, the project functions are specified at each stage. The process is repeated until definition of subtasks and algorithms solutions of which are obvious.

## Mechanism of the Algorithms Reuse

Selection of the blocks solving independent subtasks allows for their repeated application in the similar tasks. Creation of libraries of universal functions represents development of idea of usage of earlier created algorithms.

The *derived components* are tools for creation of such functions in Studio. Having once created the "[ABC analysis](https://wiki.loginom.ru/articles/abc-analysis.html)" component, it can be applied both for solution of the goods and customer base segmentation task. The subtask solved by the address check component can be applied both for data cleansing and scoring tasks.

The *inheritance mechanism* is executed in the derived components. Its advantage is its ability to modify the universal component created by a user only in one place - in the library of functions. These changes will be automatically introduced in all workflows where it is used.

However, it is not always possible to insert the universal component into particular workflow without introduction of changes into it. At the same time, it is not possible to change it in the library of functions because the inheritance mechanism will be activated. It can cause errors in all workflows where it is applied.

This task is solved by the *overriding mechanism* providing modification of the derived component only in the workflow using it. It will be unchanged in the library of functions.

## Decomposition

The Project structure can be represented in the hierarchical form:

* The Project can consist of interconnected Packages. It is possible due to the fact that *each package can provide its objects to other packages* using the mechanism of references.
* The package includes the Modules - the package decomposition on the level of modules.
* The **Module** as such does not contain data processing nodes, but it provides separate space for the Workflows and [Connections](../integration/connections/README.md) to different data sources.
* The **Workflow** contains sequence of data processing nodes. The Workflow can be distinguished by the following features:
   * It can include subprograms — the [Supernode](../processors/control/submodel.md).
   * It can receive data from nodes from other workflows and packages using the [Reference Node](../processors/control/unit-link.md) mechanism.
   * It can use settings and trained models of nodes from different workflows and packages using the [Node Execution](../processors/control/execute-node.md) mechanism.
   * It can use ready algorithms of processing of the data created in other workflows and packages using the [Derived Components](../scenario/derived-component.html) mechanism.
* The **Supernode** includes other nodes providing in such a way separate space for execution of the random algorithm of data processing. The supernode in the workflow is represented as the node that has the input and output ports set by a user. It can include hierarchy of nested supernodes. The Derived Component can be created on the supernode base.
