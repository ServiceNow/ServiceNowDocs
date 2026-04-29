---
title: Use Cloud Root Cause Analysis reports
description: Root Cause Analysis reports help you troubleshoot issues with Cloud Provisioning and Governance. Use the reports to view details about the Cloud Orchestration Trail and the Cloud API Trail.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Use Cloud Root Cause Analysis reports

Root Cause Analysis reports help you troubleshoot issues with Cloud Provisioning and Governance. Use the reports to view details about the Cloud Orchestration Trail and the Cloud API Trail.

## Before you begin

Role required: sn\_cmp.cloud\_operator or sn\_cmp.cloud\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Operate** &gt; **Root Cause Analysis Dashboard**.

    The Root Cause Analysis dashboard appears, with the **Cloud Root Cause Analysis Dashboard** displayed by default. This gives you a graphical summary of the Cloud Orchestration Trail with trail records under the reports. These charts group records by different attributes:

    -   **Trails**: groups data by the template, which is the component, such as a resource block or blueprint, on which a Cloud Provisioning and Governance action was applied.
    -   **Stages**: groups data by the stage, which identifies when the transaction took place.
    -   **Components**: groups data by the component in the system that was involved in the transaction.
    -   **Steps**: groups data by the step, which is the descriptive step associated with a stage and component.
    See [The Cloud Orchestration Trail](../concept/cloud-orch-trail.md) for a list of possible steps.

    Requests are also broken down by requester in the bar chart below. Stacks are broken down by datacenters.

    ![The Cloud Root Cause Analysis dashboard](../image/cloud-root-cause-analysis.png "The Cloud Root Cause Analysis dashboard")

2.  Select an option to obtain the tag data that you want on the report.

    |Goal|Do this|
    |----|-------|
    |**Filter the data**|Select from the options, such as the **Level**, **Date**, and the **Request Item**.|
    |**See updated data**|Point to the top of any of the charts until the refresh icon \(![Refresh icon](../image/icon-refresh.png)\) appears, and then click the icon.|
    |**Save an image of a chart**|Point to any of the charts until the options icon \(![Options icon](../image/icon-options.png)\) appears, and then select **Save as PNG** or **Save as JPEG**.|

3.  Click any Cloud Orchestration API **Number** to view that specific record.

    See [The Cloud Orchestration Trail](../concept/cloud-orch-trail.md) for field descriptions.

4.  To view reports about the Cloud API Trail, click the **Cloud API Dashboard** tab.

    This dashboard shows you several reports for the Cloud API Trail grouped by provider, status, and connectors. You can also see information the methods that were invoked and the API invocations today.

    **Note:**

    Starting with Australia the Cloud API dashboard will be hidden and no longer activated on new instances but will continue to be supported. The Cloud Services Catalog application provides this functionality now. The application is being prepared for future deprecation.

    ![The Cloud API dashboard](../image/cloud-api-dashboard.png "The Cloud API dashboard")

5.  Click any the data in the graphs to open the matching Cloud API Trail records.

    See [The Cloud API Trail](../concept/cloud-api-trail.md#) for descriptions of the Cloud API Trail form fields.


