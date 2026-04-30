---
title: insertMultiple
description: Creates multiple new records for the table targeted in the URL.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Data modification, API functions, Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# insertMultiple

Creates multiple new records for the table targeted in the URL.

## Input fields

The insertMultiple element may contain 1 or more record tags that contains all fields from the targeted table, excluding system fields. Limit the number of records inserted in a single operation to no more than 200. You can gradually increase this number with subsequent exports if the increase does not negatively impact instance performance.

## Output fields

The `insertMultipleResponse` tag is followed by 1 or more record tags that contains:

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
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:inc="http://www.service-now.com/incident">
   <soapenv:Header/>
   <soapenv:Body>
      <inc:insertMultiple>
         <record>
            <short_description>this is test 1</short_description>
         </record>
         <record>
            <short_description>this is test 2</short_description>
         </record>
         <record>
            <short_description>this is test 3</short_description>
         </record>
      </inc:insertMultiple>
   </soapenv:Body>
</soapenv:Envelope>
```

The resulting response looks like this:

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:inc="http://www.service-now.com/incident">
   <soapenv:Header/>
   <soapenv:Body>
      <insertMultipleResponse>
         <insertResponse>
            <sys_id>168160ad4a36231200a89091281dc803</sys_id>
            <number>INC0055180</number>
         </insertResponse>
         <insertResponse>
            <sys_id>1681622e4a36231200a8909115e5c388</sys_id>
            <number>INC0055181</number>
         </insertResponse>
         <insertResponse>
            <sys_id>1681626e4a36231200a89091fa3c0aa8</sys_id>
            <number>INC0055182</number>
         </insertResponse>
      </insertMultipleResponse>
   </soapenv:Body>
</soapenv:Envelope>
```

## Sample SOAP messages for an import set table

The following example shows an insert that specifies the short description only:

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:imp="http://www.service-now.com/imp_notification">
   <soapenv:Header/>
   <soapenv:Body>
      <imp:insertMultiple>:-->
         <imp:record>
            <imp:message>one</imp:message>
            <imp:uuid>a</imp:uuid>
         </imp:record>
         <imp:record>
            <imp:message>two</imp:message>
            <imp:uuid>b</imp:uuid>
         </imp:record>
         <imp:record>
            <imp:message>three</imp:message>
            <imp:uuid>c</imp:uuid>
         </imp:record>
      </imp:insertMultiple>
   </soapenv:Body>
</soapenv:Envelope>
```

The resulting response looks like this:

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:imp="http://www.service-now.com/imp_notification">
   <soapenv:Header/>
   <soapenv:Body>
      <insertMultipleResponse>
         <insertResponse>
            <sys_id>1296b3ab0a0a0b5b73e966fbfab7acde</sys_id>
            <table>incident</table>
            <display_name>number</display_name>
            <display_value>INC0010033</display_value>
            <status>ignored</status>
            <status_message>No field values changed</status_message>
         </insertResponse>
         <insertResponse>
            <sys_id>1296b48e0a0a0b5b62513bb5974a7d96</sys_id>
            <table>incident</table>
            <display_name>number</display_name>
            <display_value>INC0010034</display_value>
            <status>ignored</status>
            <status_message>No field values changed</status_message>
         </insertResponse>
         <insertResponse>
            <sys_id>1296b58b0a0a0b5b468f534659538b9a</sys_id>
            <table>incident</table>
            <display_name>number</display_name>
            <display_value>INC0010035</display_value>
            <status>ignored</status>
            <status_message>No field values changed</status_message>
         </insertResponse>
      </insertMultipleResponse>
   </soapenv:Body>
</soapenv:Envelope>
```

**Parent Topic:**[Data Modification API](r_DataModificationAPI.md)

