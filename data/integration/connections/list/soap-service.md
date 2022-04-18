# ![ ](../../../images/icons/data-sources/web-soap_default.svg) SOAP Service Connection

Loginom gives an opportunity to connect to the external SOAP service and import the data provided by it for further processing and analysis.

## Connection Parameters

The following parameters are set during the connection setup:

* **Authorization Type** provides a drop-down list with authorization options.
   * **Not required**: when selecting this option, Loginom does not perform authorization when connecting to the service.
   * **Username and password**: this option is selected if authorization by name/password is required by SOAP service for work.
   * **OAuth token** is selected when connecting to SOAP service via [OAuth](https://ru.wikipedia.org/wiki/OAuth) protocol.
   * **Provide client certificate** is selected for SSL authorization using the certificate.
* **Username**: the field becomes active if *Username and password* type is selected. The name set by a user during his registration in the SOAP service system is used for authorization.
* **Password**: the field becomes active if *Username and password* type is selected. The password set by a user during his registration in the SOAP service system is used for authorization.
* **OAuth token**: the field becomes active if *OAuth token* type is selected. The authorization process is implemented via OAuth protocol that grants rights to one service (application) to get access to the user resources available in another service. For example, authorization via social networks.
* **Certificate store**: the drop-down list that will be available when selecting *Provide client certificate*. One of the certificate stores available in the system is selected from the list. Then it is required to select the certificate used for authorization in the table below the list.
* **WSDL source**: URL or path (in file storage) of WSDL file with the service description is specified in this field.
* **Enable reserve WSDL source**: when selecting this checkbox, *Reserve WSDL source* is enabled.
   * **Reserve WSDL source**: the reserve WSDL source is specified. It will be used by the application if the main source is not available, or if errors occur while parsing the main WSDL.
* **Transform WSDL description using XSLT**: selection of this checkbox enables to introduce changes into the received WSDL file using XSLT transformation.
   * **XSLT path**: URL or path (in file storage) of XSLT file is specified in this field.
* **Connection timeout (ms)**: the maximum timeout of server response wait expressed in milliseconds upon expiration of which the access will be terminated with an error status providing that there is no response.
* **Data exchange timeout (ms)**: the maximum timeout of data wait from server expressed in milliseconds upon expiration of which the access will be terminated with an error status providing that there is no response.
* **Ignore SSL certificate errors**: when SSL connecting, the server certificate can fail the test due to some reasons. If this checkbox is selected, errors caused by untested certificate are ignored, otherwise connection will not be established.

## Authorization for Request Execution

* **Authorization is the same as for WSDL**: when this checkbox is selected, the same authorization parameters are used as for WSDL. If the request authorization differs from the WSDL authorization, it is required to deselect the checkbox and set the required parameters. Options are similar to *Authorization Type* settings from *Connection parameters*.

## Node Description

* **Caption** contains the connection name set by a user.
* **Comment**: it is possible to provide any reference data concerning connection in this form.
