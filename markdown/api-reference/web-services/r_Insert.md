---
title: insert
description: Creates a new record for the table targeted in the URL.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data modification, API functions, Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# insert

Creates a new record for the table targeted in the URL.

## Input fields

All fields from the targeted table, excluding system fields. Fields configured as mandatory in the System Dictionary are reflected in the WSDL with the attribute `minOccurs=1`.

## Output fields

<table id="table_insert"><thead><tr><th>

Table type

</th><th>

Output fields

</th></tr></thead><tbody><tr><td>

Regular

</td><td>

The **sys\_id** field and the display value of the target table \(`table`\) are returned.

</td></tr><tr><td>

Import set

</td><td>

The **sys\_id** of the import set row, the name of the transformed target table \(`table`\), the **display\_name** for the transformed target table, the **display\_value** of the transformed target row, and a **status** field, which can contain **inserted**, **updated**, or **error**.

 There can be an optional **status\_message** field or an **error\_message** field value when `status=error`.

 When an insert did not cause a target row to be transformed \(skipped because a key value is not specified\), the **sys\_id** field will contain the sys\_id of the import set row, rather than the targeted transform table.

</td></tr><tr><td>

Import set with multiple transforms

</td><td>

The response from this type of insert will contain multiple sets of fields from the regular import set table insert wrapped in a `multiInsertResponse` parent element. Each set will contain a **map** field, showing which transform map created the response.

</td></tr></tbody>
</table>## Sample SOAP messages for a regular table

The following example shows an insert that specifies the short description only:

```
<?xml version="1.0" encoding="ISO-8859-1"?>
<SOAP-ENV:Envelope xmlns:tns="http://www.service-now.com/incident" 
  xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/" 
  xmlns:m="http://www.service-now.com"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
    <SOAP-ENV:Body>
        <insert xmlns="http://www.service-now.com">
            <short_description xsi:type="xsd:string">This is a test</short_description>
        </insert>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

The resulting response looks like this:

```
<?xml version="1.0" encoding="ISO-8859-1"?>
<SOAP-ENV:Envelope SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" 
  xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/" 
  xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:m="http://www.service-now.com" 
  xmlns:tns="http://www.service-now.com/incident" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <SOAP-ENV:Body>
        <insertResponse xmlns="http://www.service-now.com">
            <sys_id>6b06494fc611227d00b5f87caf618831</sys_id>
        </insertResponse>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

## Language-specific sample messages

For language-specific insert samples, refer to the following topics:

[Perl SOAP::Lite](../../examples/concept/c_PerlWebServicesClientExamples.md#insert)

[Java Apache Axis2](../../examples/concept/c_JAAWbSrvcsClntExInst.md)

[Python](../../examples/concept/c_PythonWebServicesClientExamples.md#insert)

**Parent Topic:**[Data Modification API](r_DataModificationAPI.md)

