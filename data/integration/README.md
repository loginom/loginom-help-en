# Integration

The integration mechanisms are designated for data exchange between the third party external systems and Loginom platform. Loginom can work both with [web services](./web-services/README.md), databases and file data warehouses (spreadsheets, text files, etc.).

> **Important**:
> To provide integration with several sources, for example, databases and web services, it is required to preset [connection](./connections/README.md).

To describe the data exchange process, several sections can be identified:

* [Connnection](./connections/README.md). This section includes description of connections with parameters of access to the external systems that are required for the subsequent multiple use.
* [Import](./import/README.md). The section is designated for description of the nodes used for data retrieval from the external sources for their further processing.
* [Export](./export/README.md). The section is designated for description of the nodes used for filling the external systems with the processed data for their further storage, use, transfer or publication.
* [Web services](./web-services/README.md). This section describes Loginom and web services operation.