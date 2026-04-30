---
title: View an audit result in the Compliance view
description: After an audit has run, you can view the results and follow-on tasks from the Compliance view in the records of every CI audited.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Certification audit results, Certification audits, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View an audit result in the Compliance view

After an audit has run, you can view the results and follow-on tasks from the Compliance view in the records of every CI audited.

## Before you begin

Role required: none

## About this task

This view is available only for systems that use the default CI classes provided with the base ServiceNow system, such as Hardware, Software, and Computer. For information about creating views, see View Management.

## Procedure

1.  Navigate to **All** &gt; **Configuration** and open the record of a CI that was included in a compliance audit.

2.  Select the view to configure by performing the appropriate action for your list version.

    |Version|Action|
    |-------|------|
    |**List V2**|Open the context menu and select **View** &gt; **Compliance**.|
    |**List v3**|Open the context menu and select **Change View**, and then click **Compliance**.|

    The Audit Results Compliance View appears.

    |Lists|Description|
    |-----|-----------|
    |Passed Audit Results|Lists audits for this CI that passed without discrepancies. The information includes the versions of the template and filter used. Records are grouped first by audit, and then by creation date and time.|
    |Failed Audit Results|Lists all failed audits for this CI. The information includes the discrepancy data, the follow-on task, and the versions of the template and filter used. Records are grouped first by audit, and then by creation date and time.|
    |Follow On Tasks|Lists all follow-on tasks generated from audit discrepancies for this CI.|

3.  Right-click the header bar and select **View** &gt; **Compliance** from the context menu.


