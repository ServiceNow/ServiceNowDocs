---
title: Create SLOs, SLIs, and error budget policies
description: Define service level objectives \(SLOs\), service level indicators \(SLIs\), and error budget policies to monitor service health. These tools help you and your teams track performance and take action when needed.
locale: en-US
release: yokohama
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: task
last_updated: "2025-04-08"
reading_time_minutes: 3
breadcrumb: [Using SLO Management, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Create SLOs, SLIs, and error budget policies

Define service level objectives \(SLOs\), service level indicators \(SLIs\), and error budget policies to monitor service health. These tools help you and your teams track performance and take action when needed.

## Before you begin

If you plan to notify teams when an error budget policy is breached, make sure a notification destination is available for your team. To check, navigate to **Teams** &gt; **\[Your team\]** &gt; **SLO Notification destinations** in Service Operations Workspace.

To create a notification destination, see [Create a notification destination in SRM](create-notification-destination.md).

Role required: srm\_admin, srm\_manager, or srm\_responder

## About this task

Create SLOs, SLIs, and error budget policies to monitor service health and help make sure your services support business goals.

-   SLOs are specific targets that you set for SLIs. They define the expected performance level.
-   SLIs are metrics that measure performance, such as availability or latency.
-   Error budget policies define the acceptable margin of error and what happens if that threshold is breached.

In Service Reliability Management \(SRM\), an SLO must have at least one SLI. SLIs can be filtered to a service or configuration item \(CI\) within the parent service's hierarchy. Filtering an SLI to a CI can help you more accurately track service health and identify root causes faster.

For more high-level information about SLOs, SLIs, and error budget policies in SRM, see [Working with reliability metrics](../concept/sr-work-SLI-SLO.md).

**Note:** In SRM, each SLI can only be associated with one SLO. Using the same SLI in multiple SLOs creates multiple objectives for the same metric, which can lead to confusion or conflicting performance expectations.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  From the primary navigation, select the **Services** icon \(![Services icon](../../service-reliability/image/icon-sr-services.png)\).

3.  On the **Services** page, select the service for which you want to create SLOs and SLIs.

4.  Select the **Reliability metrics** tab and then select **Add SLO &amp; SLI**.

5.  In the Service Level Objective \(SLO\) form, fill in the fields for your SLO.

    For information about the SLO fields, see [Create SLO form](../../service-reliability/reference/sr-create-slo-sli-form.md).

6.  In the Service Level Indicators \(SLI\) form, select **Add SLI**, and fill in the fields for your SLI.

    For more information about the SLI fields, see [Create SLI form](../../service-reliability/reference/sr-create-sli-form.md).

    **Note:** If your service includes one or more CIs in its hierarchy, a banner appears below the Service Level Indicators \(SLI\) header. The banner lists the number of available CIs and links to the service map, letting you visualize their connections. You can use this information to filter your SLIs to specific CIs in the Add SLI form, giving you a more granular measure of service health.

7.  In the Error budget policies form, select **Add threshold**, and fill in the fields for your error budget policy.

    For more information, see [Add an error budget policy form](../reference/sr-create-error-budget-form.md).

    **Note:** If you don't add an error budget policy, the SLO's objective percentage is only informational. Adding a policy helps you take corrective actions based on the performance data. If you're not ready to add a policy now, you can add one later.

8.  Review your SLO, SLI, and error budget policy, and then select **Activate**.

    Your SLO, SLI, and, if added, error budget policy are active, helping you monitor service health and take action when necessary. For information about viewing and updating reliability metrics, see [Edit a reliability metric](sr-edit-sli-slo.md).


**Parent Topic:**[Using SLO Management](using-service-level-objective-management.md)

