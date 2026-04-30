---
title: Creating an import set web service
description: Create a web service import set table to define how to stage and transform imported data.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Web service import sets, Import sets, Imports, Data and Automation]
---

# Creating an import set web service

Create a web service import set table to define how to stage and transform imported data.

Navigate to **All** &gt; **System Web Services** &gt; **Inbound** &gt; **Create New**.

![](../image/CreateMappedWebService.jpg "Create Web Service")

The Name of the web service is the table name of the import set table whereas the Label field is the resulting table field.

If you want to create a transform map after creating the web service, check the **Create transform map** checkbox and choose the target table you want the data to transform into. After the **Create** button is selected, the web service is created and you will be immediately put into the Table Transform Map form. You may then continue to specify the transform map or script.

## Web Service Fields

The fields available for this web service. All fields by default are published as the XSD type of `xsd:string`. The Name is the field that is exposed for the web service and therefore appears as the name of the field in the WSDL. The Label is the label of the field as it appears for the import sets table.

You can Add, mark for Delete or modify \(double-click the field\) an existing web service field in this list.

**Note:** After adding web service fields, click **Create** to create the web service import set table.

To add other fields after the Web Service is created, find the target table, and add the fields to that table.

## Mapping web service import sets

During the creation of the web service import set, you may optionally create the transform map for it.

All transform maps are executed for the service when it is invoked and the import set mode is set as "Synchronous" \(the default\).

The following image is an example of the transform map associated with the Notification web service import set.

![](../image/SoapTransformMap.jpg "Notification Transform Map")

## Adding Web Service Response Values

In the transform map script associated with a web service import set, some variable values can change the response values of the web service. In addition to the normal variables that are available in a transform map script, the table documents the variables that are available and their effects.

|Variable name|Type|Description|
|-------------|----|-----------|
|response|Output Object|Javascript object that holds dynamically created response elements used to customize the output response of a web service import set insert.|

**Example**

```
// create new elements called "transaction_id" 
// and "hello" in the web service response
response.transaction_id="abc123";
response.hello="world";
 
status_message="message 1";
// this is the normal status_message variable
```

The code snippet example results in the following response being generated back to the web service consumer

```
<soapenv:Envelopexmlns:imp="http://www.service-now.com/imp_notification"                  
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
<soapenv:Header/><soapenv:Body>
<insertResponse xmlns="http://www.service-now.com/imp_notification">
  <sys_id>969d157c0a0a0baf008ba5770ffa798c</sys_id>
  <table>incident</table>
  <display_name>number</display_name>
  <display_value>INC0010091</display_value>
  <status>inserted</status>
  <status_message>message 1</status_message>
  <transaction_id>abc123</transaction_id>
  <hello>world</hello>
</insertResponse>
</soapenv:Body></soapenv:Envelope>
```

## Debugging web service import sets

To debug a SOAP Request coming into the system, create the system property glide.processor.debug.SOAPProcessor.

Once you have created it, set it to true to have all SOAP requests be logged in the System Log. Set it to false when you are done to keep the size of your System Log to a managed length.

**Parent Topic:**[Web service import sets](c_WebServiceImportSets.md)

