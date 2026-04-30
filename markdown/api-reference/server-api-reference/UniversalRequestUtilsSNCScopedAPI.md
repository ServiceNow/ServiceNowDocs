---
title: UniversalRequestUtilsSNC - Scoped
description: The UniversalRequestUtilsSNC API enables handling universal request life cycles. Provided as a script include record.Creates a universal request and returns the sys\_id of the newly created universal request record.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# UniversalRequestUtilsSNC- Scoped

The UniversalRequestUtilsSNC API enables handling universal request life cycles. Provided as a script include record.

This API requires the Universal Request \(com.snc.universal\_request\) plugin and is provided within the `sn_uni_req` namespace.

For information, refer to [Universal Request](https://www.servicenow.com/docs/access?context=ur-landing-limitedaccess&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## UniversalRequestUtilsSNC - createUniversalRequest\(Object copyFields\)

Creates a universal request and returns the sys\_id of the newly created universal request record.

This method is called using the UniversalRequestUtils prototype in the `sn_uni_req` namespace. For example, `sn_uni_req.UniversalRequestUtils().createUniversalRequest(<copyFields>)`.

<table id="table_agv_xrd_gnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

copyFields

</td><td>

Object

</td><td>

JSON object containing field names and values to set on a new record in the Universal Requests \[universal\_request\] table.Provide details by field name and field value in the format `{ '<field_name>': '<field_value>' }`. The following fields are considered the most useful details to assign to a primary ticket.

```

{
  'assignment_group': 'String',
  'assigned_to': 'String',
  'contact_type': 'String',
  'description': 'String',
  'opened_by': 'String',
  'opened_for': 'String',
  'priority': 'String',
  'restricted': Boolean,
  'short_description': 'String'
};
```

Other fields not listed might be eligible for your use case. For a list of table fields and related fields in the system, view the [Data dictionary tables](https://www.servicenow.com/docs/access?context=c_DataDictionaryTables&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Note:** Do not include the primary\_ticket or sys\_id fields in the copyFields JSON object.

</td></tr><tr><td>

copyFields.assignment\_group

</td><td>

String

</td><td>

Optional. Sys\_id of the group assigned to the resource.Default: Default assignment group is set per assignment rules.

Table: Group \[sys\_user\_group\] table.

</td></tr><tr><td>

copyFields.contact\_type

</td><td>

String

</td><td>

Optional. Method by which the resource was initially reported.Possible values:

-   chat
-   email
-   phone
-   social
-   web

Maximum length: 40

</td></tr><tr><td>

copyFields.description

</td><td>

String

</td><td>

Optional. Detailed description of the problem associated with the resource.Maximum length: 4,000

</td></tr><tr><td>

copyFields.opened\_by

</td><td>

String

</td><td>

Optional. Sys\_id of the person that initially opened the resource. Located in the User \[sys\_user\] table.

</td></tr><tr><td>

copyFields.opened\_for

</td><td>

String

</td><td>

Optional. Required for HR Service Delivery cases. The sys\_id of the user for whom the resource was opened.

</td></tr><tr><td>

copyFields.priority

</td><td>

String

</td><td>

Optional. Priority of the resource. Specified as a number.Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Default: 3

</td></tr><tr><td>

copyFields.restricted

</td><td>

Boolean

</td><td>

Optional. Flag that indicates if the universal request has restricted access. Refer to [Universal Request roles and groups](https://www.servicenow.com/docs/access?context=ur-roles&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

 Valid values:

-   true: Universal request is only accessible to users with the `sn_uni_req.sensitiveinfo_agent` role. Users with this role have permissions to view sensitive information, such as payroll details.
-   false: Universal request access is unrestricted.

 Default: false

</td></tr><tr><td>

copyFields.short\_description

</td><td>

String

</td><td>

Concise description of the resource.Maximum length: 160

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Sys\_id of the newly created universal request record.|

The following example shows how to set fields on a new universal request. In this use case, this code is added to the beginning of the Inbound Email Actions \[sysevent\_in\_email\_action\] scoped **Create HR Case** script. If the case doesn't apply to HR, agents can transfer the case to the appropriate department.

```
var copiedFields = {
  'opened_for': "<user_sys_id>",    
  'short_description': email.subject,
  'restricted': false,
  'priority': '1'
};

// createUniversalRequest() must be called to create the universal request prior to creating the child case

var ur = new sn_uni_req.UniversalRequestUtils().createUniversalRequest(copiedFields);
current.universal_request = ur;

```

