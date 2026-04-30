---
title: Defining Name Components
description: Name components define the document values used in the name format.
locale: en-US
release: xanadu
product: Document Management Services
classification: document-management-services
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Defining Document Parameters, Features, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Defining Name Components

Name components define the document values used in the name format.

For example, the name component `document.audience.code` dot-walks from the document record to the audience **Code**.

To define a new name component, navigate to **Managed Documents** &gt; **Administration** &gt; **Components** and click **New**.

<table id="table_zgf_ksc_s4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique identifier for the name component.

</td></tr><tr><td>

Short Description

</td><td>

A short description of the name component value.

</td></tr><tr><td>

Value

</td><td>

The path to the field holding the value used for the name format. Defined relative to a current revision record.For example:

-   Enter `revision` to use the revision **Number** field on the revision record.
-   Enter `document.name` to use the **Name** field on the revision's referenced document.
-   Enter `document.audience.code` to use the **Code** field for the audience referenced by the document.

 This dot-walking approach makes it possible to get any value related to the revision into the name format.

</td></tr></tbody>
</table>**Note:** The **revision** component is a special component replaced by the appropriate revision number \(rather than querying a value related to the current record\). The revision is either automatically incremented or uses the latest revision number, depending on the setting on the document form.

The following components are defined in the base system.

|Name|Short description|Value|
|----|-----------------|-----|
|Audience code|Displays the code assigned to the document audience.|document.audience.code|
|Classification code|Displays the classification code.|document.classification.code|
|Document name|Displays the document name.|document.name|
|Revision|Displays the document revision.|revision|
|Type code|Displays the code assigned to the document type.|document.type.code|

**Parent Topic:**[Defining Document Parameters](r_DefiningDocumentParameters.md)

