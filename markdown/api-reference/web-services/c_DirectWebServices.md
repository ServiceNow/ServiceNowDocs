---
title: Direct web services
description: A direct web service is available for any table in the system if the correct access control list is configured.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Direct web services

A direct web service is available for any table in the system if the correct access control list is configured.

The supported format of the incoming message is document style literal XML SOAP documents \(Document/Literal\). To retrieve a direct web service WSDL description and XML schema, point to the relative URL `<tablename>.do?WSDL`. For example, to retrieve the WSDL for the Incident table on the online demo system, use the following URL: `https://<instance name>.service-now.com/incident.do?WSDL`.

## Extended query parameters

Extended query parameters enable you to filter and modify the return results of a SOAP query when using the get, getKeys, and getRecords functions.

**Note:** Extended query element names are preceded by two underscore characters.

|Parameter|Description|Example|
|---------|-----------|-------|
|\_\_encoded\_query|Specify an encoded query string to be used in filtering the returned results. The encoded query string format is similar to the value that may be specified in a `sysparm_query` URL parameter. See the encoded query building example in the RSS feed generator examples.|`<__encoded_query>active=true^category='hardware'</__encoded_query>`|
|\_\_order\_by|Instruct the returned results to be ordered by the specified field.|`<__order_by>priority</__order_by>`|
|\_\_order\_by\_desc|Instruct the returned results to be ordered by the specified field, in descending order.|`<__order_by_desc>opened_date</__order_by_desc>`|
|\_\_exclude\_columns|Specify a list of comma delimited field names to exclude from the result set.|`<__exclude_columns>sys_created_on,sys_created_by,caller_id,priority</__exclude_columns>`|
|\_\_limit|Limit the number of records that are returned.|`<__limit>100</__limit>`|
|\_\_first\_row|Instruct the results to be offset by this number of records from the beginning of the set. When used with `__last_row` has the effect of querying for a window of results. The results are inclusive of the first row number.|`<__first_row>250</__first_row>`|
|\_\_last\_row|Instruct the results to be limited by this number of records from the beginning of the set, or the `__start_row` value when specified. When used with `__first_row` has the effect of querying for a window of results. The results are less than the last row number, and does not include the last row.|`<__last_row>500</__last_row>`|
|\_\_use\_view|Specify a Form view by name, to be used for limiting and expanding the results returned. When the form view contains deep referenced fields such as **caller\_id.email**, this field will be returned in the result as well.|`<__use_view>soap_view</__use_view>`|

## Direct web services namespace

## Specifying a unique namespace for each table

The **glide.wsdl.definition.use\_unique\_namespace** property ensures that each table's direct web service WSDL has a unique **targetNamespace** attribute. This property is **true** by default, which requires a table's direct web service WSDL to use a **targetNamespace** value of `http://www.service-now.com/<table name>`. When **false** \(or when the property is not present\), all tables use the same **targetNamespace** value of `http://www.service-now.com`. Since all tables also share the same operation names, a web service client attempting to consume more than one ServiceNow web service would be unable to differentiate between requests between multiple tables. Using a unique **targetNamespace** value allows web service clients to distinguish requests between multiple tables.

For example, the direct web service WSDL for the incident table uses this **targetNamepsace** value:

```
<wsdl:definitions xmlns:soapenc= "http://schemas.xmlsoap.org/soap/encoding/"xmlns:wsdl = "http://schemas.xmlsoap.org/wsdl/"xmlns:http = "http://schemas.xmlsoap.org/wsdl/http/"xmlns:tns = "http://www.service-now.com/incident"xmlns:xsd = "http://www.w3.org/2001/XMLSchema"xmlns:mime = "http://schemas.xmlsoap.org/wsdl/mime/"xmlns:soap = "http://schemas.xmlsoap.org/wsdl/soap/"targetNamespace = "http://www.service-now.com/incident" ><wsdl:types><xsd:schema elementFormDefault = "unqualified"targetNamespace = "http://www.service-now.com/incident" >
```

## Setting namespace requirements

ServiceNow's WSDL schema by default declares an attribute of **elementFormDefault="unqualified"**. This attribute indicates whether or not locally declared elements must be qualified by the **targetNamepsace** in an instance document. If the value of this attribute is **unqualified**, then locally declared elements should not be qualified by the **targetNamepsace**. If the value of this attribute is **qualified**, then locally declared elements must be qualified by the **targetNamepsace**.

However, this is incompatible with the way clients generated from WSDL \(for example, .NET, Axis2, webMethods\) process the embedded schema. It removes the schema namespace as a result, making the web service response unparseable.

To overcome this compatibility issue, a boolean property called **glide.wsdl.schema.UnqualifiedElementFormDefault** is introduced. This property has the value of **true** by default. Setting it to **false** enables clients generated from WSDL to parse the return value of the web service invocation. You can modify this property using the Web Services properties page at **System Properties** &gt; **Web Services**.

## Allowing duplicate service names

By default, service names from dynamically generated WSDL are unique and have the following format:

```
ServiceNow_<table name>
```

To allow duplicate service names, administrators can set the **glide.wsdl.unique\_service\_name** property to **false**. Create the property if it does not exist.

-   **[Use forms to limit or extend the query response](using-forms-limit-extend-query-resp.md)**  
On occasion, there is a need to limit the number of field values that a SOAP query returns.
-   **[Return the display value for reference variables](return-display-reference-variables.md)**  
When you query a record using a **get** or **getRecords** function, the instance returns all fields associated with that record. The fields are often reference fields that contain a sys\_id for a record on another table.
-   **[Clear values from a target instance](clearing-values-target.md)**  
You can pass an empty value through a SOAP parameter to clear the respective value in the target instance.
-   **[Retrieve journal entries using direct web services](retrieving-journal-entries.md)**  
To get the contents of a journal field, make a second soap request against the sys\_journal\_field table to pull the appropriate journal records back for the record in question.
-   **[Retrieve choice fields using direct web services](retrieving-choice-fields-direct-ws.md)**  
To retrieve or set choice fields, use the choice **Value**, not the **Label**.
-   **[Persist an HTTP session across all SOAP calls](persist-session-all-soap-calls.md)**  
In circumstances when a SOAP client makes many calls in a short amount of time, you may want to re-use a single HTTP session for all SOAP calls.
-   **[SOAP direct web service API functions](../../web-services-apis/reference/r_DirectWebServiceAPIFunctions.md)**  
The standard SOAP API is a set of small, globally defined functions that can be performed on a targeted resource.

**Parent Topic:**[SOAP web service](c_SOAPWebService.md)

**Related topics**  


[SOAP web service](c_SOAPWebService.md)

