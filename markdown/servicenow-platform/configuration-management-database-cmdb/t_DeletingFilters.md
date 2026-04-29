---
title: Delete a certification filter
description: Delete certification filters that are no longer needed and no longer in use.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certification filters, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Delete a certification filter

Delete certification filters that are no longer needed and no longer in use.

## Before you begin

Role required: certification\_admin or admin

## About this task

You can't delete a certification filter that is being used in a template or a scripted audit.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**, and:

    1.  Select **Hierarchy** to show the CI Classes list.

    2.  Select the class to delete a filter for.

    3.  In the class navigation bar, expand **Health**.

    4.  Select **Compliance** and then **Certification Filter**.

2.  Or, navigate to one of these modules:

    -   **Compliance** &gt; **Filters**
    -   **Data Certification** &gt; **Schedules** &gt; **Certification Filters**
3.  Open the filter record you want to delete.

    1.  To delete a single filter version, open that version record and click **Delete**.

        The system hides the **Delete** button for filters that are in use. If you delete the latest version of a filter that is active, the previous version of that filter is reset to Active.

    2.  To delete all unused and inactive versions of a filter, open any version of that filter and click **Delete inactive versions** under **Related Links**.

4.  When prompted, select **OK** to proceed.

    The system deletes unused filter versions. A message in the header bar identifies filter versions that cannot be deleted because they are used in a template or scripted audit.


