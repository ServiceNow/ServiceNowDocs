---
title: View a reclassification task
description: Reclassification tasks are created for CIs that couldn't be automatically reclassified during the identification process. Review these tasks to locate the CIs and decide if to reclassify them.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View a reclassification task

Reclassification tasks are created for CIs that couldn't be automatically reclassified during the identification process. Review these tasks to locate the CIs and decide if to reclassify them.

## About this task

The properties you use to disable automatic CI reclassification determine whether reclassification tasks are created for those CIs that couldn't be automatically reclassified:

-   Using any one of the 'glide.class.&lt;reclassification operation&gt;.enabled' properties \(such as **glide.class.upgrade.enabled**\): Reclassification tasks are created.
-   Using any one of the 'glide.identification\_engine.update\_without\_&lt;reclassification operation&gt;\_enabled' properties \(such as **glide.identification\_engine.update\_without\_switch\_enabled**\): Reclassification tasks aren't created.

For more information about reclassification during IRE processing, see [Configure CI reclassification during IRE processing](../concept/c_CIReclassification.md#).

## Before you begin

Role required: sn\_cmdb\_admin, sn\_cmdb\_editor, admin, or itil

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **Reclassification Tasks**.

2.  Select a reclassification task.

3.  Examine the details on the Reclassification Task form.

    |Field|Description|
    |-----|-----------|
    |Configuration item|The CI that must be reclassified.|
    |Short description|Short description noting that CI reclassification was not allowed.|
    |Description|Description noting the current class of the CI and the class that the CI must be changed to.|
    |Internal payload|Payload used in the identification process.|


## What to do next

After examining the task details, you can locate the CI that is noted in the task **Description** and manually reclassify it. For details, see [Reclassify a CI](t_ManuallyReclassifyCI.md).

**Parent Topic:**[CMDB Identification and Reconciliation \(IRE\)](../concept/c_CMDBIdentifyandReconcile.md)

