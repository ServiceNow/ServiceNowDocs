---
title: Add relationship form
description: Relate a business application to an information object using the CI relationship \[cmdb\_rel\_ci\] table of type Uses::Used by. Use this suggested relationship to get the logical data of the information object to leverage a business application.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Add relationship form

Relate a business application to an information object using the CI relationship \[cmdb\_rel\_ci\] table of type Uses::Used by. Use this suggested relationship to get the logical data of the information object to leverage a business application.

## Add relationship form fields

<table id="table_yd4_qq1_fhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business Application

</td><td>

Name of the business application that auto-populates in the field.

</td></tr><tr><td>

Relationship

</td><td>

Type of suggested CMDB CI relationship between the business application and the information object. The field is auto-populated with Uses::Used by relationship.

</td></tr><tr><td>

Select Information Object

</td><td>

Table with the logical data that the business application uses.

</td></tr><tr><td>

Create, Read, Update, and Delete

</td><td>

Options for capturing the type of operation or a combination of operations that the business application can do on the information object.Selecting the Create, Read, Update, and Delete \(CRUD\) check boxes adds qualifiers, which are properties that define the extent of the relationship between the business application CI and the information object CI.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture \(formerly Application Portfolio Management\) reference](apm-reference.md)

**Related topics**  


[Manage information objects of a business application in EA Workspace](../task/eaw-task/eaw-associate-info-obj-ba.md)

[Relate a business application to an information object](../task/relate-business-app-information-object.md)

