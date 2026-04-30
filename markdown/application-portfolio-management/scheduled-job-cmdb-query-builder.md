---
title: Run scheduled jobs for CMDB Query Builder reports - Legacy
description: Schedule a job to run at a scheduled time or on a recurring schedule for CMDB query. Ensure to do this action in global scope.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Run scheduled jobs for CMDB Query Builder reports - Legacy

Schedule a job to run at a scheduled time or on a recurring schedule for CMDB query. Ensure to do this action in global scope.

## Before you begin

Role required: sys\_admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search and click the relevant scheduled job.

3.  Select the frequency at which to run the scheduled job in the **Run** field.

4.  Click **Execute Now**.

    **Note:** As a system administrator you must run these scheduled jobs from Global scope only.

    Select and run the scheduled jobs for the following CMDB Query Builder reports that the base system offers:

    -   Business Capabilities provided by Business Application
    -   Application Services consumed by Business Application
    -   Business Applications providing a Business Capability
    -   Business Services provided by a Business Capability
    -   Business Applications using an Information Object
    -   Information Objects used by a Business Application
    -   Demands on a Business Application
    -   Projects on a Business Application

**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](../concept/configure-apm.md)

