---
title: Create SLO, SLI, and Error budget policies
description: Create SLO, SLI, and Error budget policies to help you and your team track your service health and take the necessary actions when required.
locale: en-US
release: xanadu
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working with Reliability metrics, Using SLO Management, Service Level Objective Management, ITOM Health, IT Operations Management]
---

# Create SLO, SLI, and Error budget policies

Create SLO, SLI, and Error budget policies to help you and your team track your service health and take the necessary actions when required.

## Before you begin

Role required: Responder, Manager, or Administrator

## About this task

**Note:** You can set up only one SLO for an SLI.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You are taken to your SRM homepage.

    **Note:** If you have other SOW applications, and depending on your assigned roles, that homepage may not be the SRM homepage. It is the SOW homepage instead, with SRM alerts and incidents included in your metrics. In that case, to view SRM specific areas, select SRM modules from the left navigation pane.

2.  From the left navigation pane, select the services icon \(![Services icon](../../service-reliability/image/icon-sr-services.png)\).

3.  On the **Services** page, open the service for which you want to create SLO and SLI.

4.  Select the **Reliability metrics** tab.

5.  Select **Add SLO &amp; SLI**.

    The service level objective is the objective your team must hit to meet the service level agreement \(SLA\). It's your goal.

    The Set up reliability metric tab opens.

6.  In the Service-level objective \(SLO\) form, fill in the appropriate fields.

    For more information, see [Create SLO form](../../service-reliability/reference/sr-create-slo-sli-form.md).

    **Note:** You’re defining a time period for compliance and a goal for reliable service.

7.  In the Service-level indicators \(SLI\) form, select **Add SLI** and fill in the appropriate fields.

    For more information, see [Create SLI form](../../service-reliability/reference/sr-create-sli-form.md).

    **Note:** An SLI is a quantitative measure of some aspect of the level of service that is provided. These metrics are used to define SLO targets. At least one SLI is required.

8.  In the Error budget policies form, select **Add threshold** and fill in the appropriate fields.

    For more information, see [Create Error budget policies form](../reference/sr-create-error-budget-form.md).

    An error budget is the amount of SLO that you can spend over a specified time. SRM aims to minimize error budget consumption to maximize reliability.

    **Note:** If you don't choose to add an error budget policy now then **Objective \(percentage\)**, which triggers actions, remains informational. Creating one gives you some remediation options.

    You can add an error budget policy later by opening the SLO and selecting the **Error budget policies** tab.

    **Note:** The header in your **Error budget policies** pane will update depending on whether you chose **Duration** or one of the **Count** settings for your SLO.

9.  Review your SLO, SLI, and Error budget policies.

10. Select **Activate**.

    See [Edit a reliability indicator](sr-edit-sli-slo.md) for more detailed information on the final SLO page.


**Parent Topic:**[Working with Reliability metrics](../concept/sr-work-SLI-SLO.md)

