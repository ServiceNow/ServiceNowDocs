---
title: View Service Level Agreement \(SLA\) results in Service Portfolio Management
description: Service Portfolio Management leverages the Service Level Management application and includes a module to manage your Service Level Agreement \(SLA\) definitions and results.
locale: en-US
release: zurich
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Service Portfolio Management, IT Service Management]
---

# View Service Level Agreement \(SLA\) results in Service Portfolio Management

Service Portfolio Management leverages the Service Level Management application and includes a module to manage your Service Level Agreement \(SLA\) definitions and results.

You can view, modify, or create SLA definitions from the Service Portfolio Management application. You can also view, modify, or create SLA results. Refer to [Service Level Agreement \(SLA\) definition](../../service-level-management/concept/c_SLADefinitions.md) and [Create an SLA definition](../../service-level-management/task/t_CreateAnSLADefinition.md) for information about SLA definitions and configuration. For complete detailed information about SLAs, refer to [Service Level Management](../../service-level-management/reference/service-level-mgmt-landing-page.md).

After you define service commitments for your offerings, you can monitor the SLA results to manage performance by the running a daily job that generates the SLA results.

To enable Service Level Agreement \(SLA\) commitment support to Service Portfolio Management, activate the com.snc.service\_portfolio.sla\_commitment plugin. For more information, see [Activate Service Portfolio Management](../task/activate-SPM2-plugin.md).

To view the SLA results, navigate to **Service Portfolio Management** &gt; **Service Level Management** &gt; **SLA Results**. To edit an SLA result, select the name of the SLA result to open the SLA Result form. Change any of the form field data as needed.

|Field|Description|
|-----|-----------|
|Service offering|Select the service offering for which you want to create or modify an SLA Result record.|
|Service commitment|Select the service commitment to apply the SLA Result record.|
|Start|Specify the start date for this SLA Result interval.|
|End|Specify the end date for this SLA Result interval.|
|Company|Specify the company for which the SLA Result record is created.|
|Required SLA percentage|Enter the percentage of tasks that must meet this SLA.|

**Note:** The following fields display SLA result data when available:

-   **Total tasks** — Total number of incidents that are opened against the service offering.
-   **Breached** — Number of tasks that breached this SLA for this interval.
-   **Achieved** — Number of tasks that achieved this SLA for this interval.
-   **Total achieved %** — SLA percentage achieved for the entire interval.

**Note:** When an SLA definition is triggered against a particular task, a task SLA record generates and contains all the tracking data for the specific SLA on that record. To create an SLA task or modify an existing task, refer to [Task SLA table](../../service-level-management/reference/r_TaskSLATable.md).

**Parent Topic:**[Using Service Portfolio Management](SPM2-using.md)

