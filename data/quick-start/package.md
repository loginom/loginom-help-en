# Package Designation and Structure

All actions with the project in Loginom must be performed within the Package that is a minimum delivery unit and has the form of a container for components, workflows, connections, etc.

Packages are saved separately in the form of files with .lgp extension, and they include References and Modules.

The References are used for connection of other packages in order to use the derived components created in them and connections in the current project. Corresponding objects are available only if they are published for shared access.

Each package contains at least one module. The Module inludes the following items:

* The [Workflow](./first-scenario.md) contains sequence of data processing nodes.
* [Connections](./../integration/connections/README.md) include a list of the external sources and data receivers to be connected with.
* [Components](./../processors/README.md#standartnye-komponenty) include the supernodes available for work, both created within the current package and borrowed from other packages using references.

> Note: in the case of any package opening the file with the following name is created: `<Package_name>.lgp.lck`. This file protects the opened package from possible editing or deleting by other users. This file is deleted upon the package closure.
