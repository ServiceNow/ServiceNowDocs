---
title: Configure scheduled jobs in the Configuration Console
description: Automate recurring SAM processes such as normalization, reconciliation, and cleanup operations by configuring scheduled jobs in the Configuration Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/manage-scheduled-jobs-sam-using-config-console.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure SAM using Configuration Console, Configuration Console for Software Asset Management, Software Asset Management installation methods, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Configure scheduled jobs in the Configuration Console

Automate recurring SAM processes such as normalization, reconciliation, and cleanup operations by configuring scheduled jobs in the Configuration Console.

## Before you begin

Install the Software Asset Management application. For installation instructions, see [Install Software Asset Management from the Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-sam-product-hub.md).

Role required: system\_scheduler\_admin

## About this task

The Configuration Console displays only jobs specific to Software Asset Management.

## Procedure

1.  In the Configuration Console, navigate to **Governance** &gt; **Scheduled jobs**.

    The Scheduled jobs page displays a pre-filtered list of Software Asset Management jobs.

2.  Select a job name to view its details.

    Filter, sort, or group the list to locate a specific job. The list displays each job with its name, active state, class, and last updated timestamp.

3.  To create a scheduled job for Software Asset Management, select **New**.

    1.  In the **Name** field, enter a descriptive name for the job.

    2.  Configure the schedule using the **Run**, **Time**, and **Time zone** fields.

        Specify the frequency \(daily, weekly, monthly\), time of day, and time zone.

    3.  In the **Run as** field, enter the user account that runs the job.

    4.  Select **Save**.

4.  To export the list of scheduled jobs, select **Export**.

    1.  From the **File Type** list, select the file type.

    2.  Select the delivery method: **Download** or **Email**.

    3.  Select **Export**.

5.  To mark a step as configured, select **Mark as configured**.

    The Configuration Summary page updates the setup status to reflect the completed item.


**Parent Topic:**[Configure Software Asset Management using the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-sam-from-config-console.md)

**Related topics**  


[Configuration Console overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/config-console-overview.md)

[Configuration Console for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/config-console-sam.md)

