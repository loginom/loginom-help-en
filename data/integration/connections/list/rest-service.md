# ![](../../../images/icons/data-sources/web-rest_default.svg) REST Service Connection

Parameters of the REST service connection, request and response are set. The output connection data is used by the [REST Request](../../../processors/integration/rest-request.md) node.

## Connection Parameters

* **Service URL**: address of request sending to REST service is set.
* **Method**: one of the HTTP methods used while request sending to the service is selected.
   * **GET**: when selecting this method, the following settings are available:
      * Type of the Content-type response: the REST request node that uses this connection checks the response type for consistency with the data specified in this parameter. If the types are inconsistent, the output data set of this node will contain an error message. This test is not performed in the case of the following parameter value:`*/*`.
      * GET request parameters: a list of GET request parameters, their names and data types are set. Subsequently, values are set for these parameters and the request text is generated in the node used for REST service calling.
   * **POST**: when selecting this method, the following settings are available:
      * Type of the Content-type request: the `Content-type` header value of HTTP request to REST service is set. It is allowed both to select from the list of predefined values, and to enter a random value.
      * Type of the Content-type response: the same as for GET method (refer to the information above).
* **Connection timeout (ms)**: the maximum time required for TCP server connection expressed in milliseconds upon expiration of which the connection will be terminated with an error status. If this parameter is equal to 0, timeout is not limited.
* **Data exchange timeout (ms)**: the maximum time that is required to send HTTP request and receive response upon expiration of which the exchange will be terminated with an error status. If this parameter is equal to 0, timeout is not limited.
* **Ignore SSL certificate errors**: if this checkbox is selected, the errors detected while testing the server certificate to be connected with are ignored.

## Authorization for Request Execution

* **Authorization Type** provides a drop-down list with authorization options:
   * **Not required**: when selecting this option, Loginom does not perform authorization when connecting to the service.
   * **Username and password**: this option is selected when authorization by name/password is required. The following types of authorization by username and password are supported:
      * Basic;
      * Digest;
      * NTLM;
      * Passport;
      * Negotiate.
   * **OAuth token** is selected when connecting to the web service via [OAuth](https://ru.wikipedia.org/wiki/OAuth) 2.0 protocol.
   * **Provide client certificate** is selected for SSL authorization using the certificate.
* **Username, Password**: the field becomes active if *Username and password* type is selected. When registering in the web service system, parameters of user authorization are set.
* **OAuth token**: the field becomes active if *OAuth token* type is selected. The token string is entered.
* **Certificate store**: the drop-down list that will be available when selecting *Provide client certificate*. One of the certificate stores available in the system is selected from the list. Then it is required to select the certificate used for authorization in the table below the list.