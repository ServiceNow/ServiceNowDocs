---
title: Relate a business application to an information object
description: Relate a business application to an information object using the CI relationship \[cmdb\_rel\_ci\] table of type Uses::Used by. Use this suggested relationship to get the logical data of the information object, which can be used to leverage the business application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Relate a business application to an information object

Relate a business application to an information object using the CI relationship \[cmdb\_rel\_ci\] table of type Uses::Used by. Use this suggested relationship to get the logical data of the information object, which can be used to leverage the business application.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

**Note:**

Use the custom-built Add Relationship UI to relate the business application with the information object because this UI also captures the attributes in the relationship between the two configuration items. You should not use the CMDB relationship editor to associate the two configuration items because the create, read, update, and delete \(CRUD\) attributes of the relationship cannot be captured in the relationship editor.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Application Portfolio** &gt; **All Business Applications**.

2.  Open a business application record.

3.  To relate the business application with an information object, click the Information Object Attributes related list.

4.  To add an information object, click **Add**.

5.  On the form, fill in the fields.

    For field information, see [Add relationship form](../reference/add-relationship-form.md).

    By adding an information object to the business application, not only a record is created in the CI relationship \[cmdb\_ci\_rel\] table, but the CRUD attributes are also captured in the CI Relation Attributes \[cmdb\_rel\_attributes\] table.

6.  Click **Save**.

    To edit the CRUD relationship of an information object, select the record and click **Edit**. In the Manage Relationship pop-up, update the CRUD details.

    To delete the relationship between the business application and an information object record, select the record and click **Delete Relationship**. This action deletes the relationship record from the CI relationship table and also deletes the qualifier properties, if any, that are set in this relationship between the business application and the information object, which are captured in the CI Relation Attributes table.

    To check for information objects that are not linked to any business applications, run the Information Objects not related to any Business Application desired state audit on demand. For more information, see [Information Objects not related to any Business Application](run-desired-and-scripted-audits.md#info-obj-des-audit).


## What to do next

Relate the information object to the database catalog.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)

