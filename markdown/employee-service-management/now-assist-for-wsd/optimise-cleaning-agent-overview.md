---
title: Optimize cleaning activities agent overview
description: The Optimize cleaning activities agent performs cleaning activities on a workplace location based on the space utilization threshold data.
locale: en-US
release: zurich
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2025-08-25"
reading_time_minutes: 5
breadcrumb: [Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Optimize cleaning activities agent overview

The Optimize cleaning activities agent performs cleaning activities on a workplace location based on the space utilization threshold data.

This team of AI agents get all open workplace maintenance management cases. The **Workplace Planned Maint Nightly Run** scheduled job runs on a daily or hourly basis to create maintenance cases. Each workplace maintenance case represents a cleaning or a maintenance case on a location for a certain time interval, also known as schedule \(on a daily or hourly basis\). The Optimize cleaning activities agentic AI workflow retrieves space utilization threshold for each workplace maintenance cases.

**Note:** Optimize Cleaning Activities Agentic workflow optimizes a space at the floor level for a selected building. It only optimizes non-reservable spaces like restrooms and so on.

For more information about how to create maintenance management plan records, see [Create and publish maintenance plans](../../workplace-maintenance-management/task/create-publish-maintenance-plans.md).

-   The Optimize cleaning activities agentic AI workflow is triggered when the **Optimize cleaning activities** scheduled job is executed. The Optimize cleaning activities AI agent optimizes a maintenance plan record and gets space utilization data using the following Workplace Maintenance Management properties.

    For more information, see [Components installed with Workplace Maintenance Management](../../workplace-maintenance-management/reference/components-installed-with-maintenance-mgmt.md)

    -   The **sn\_wsd\_maintenance.optimise\_plans** property helps in optimizing a maintenance plan for a selected floor. To optimize a maintenance plan, workplace maintenance managers should copy the sys\_id from the maintenance plan URL. For example, &lt;https://&lt;instance\_name&gt;.service-now.com/now/workplace-management/maintenance-plan/ 59e13dbc3b27ee5090fd390f23e45a68. You can also copy the sys\_id of a maintenance plan record by navigating to the Additional actions icon \(![Additional actions icon](../../wsd-reservation-management/image/additional-actions.png)\) and select **Copy sys\_id**.

        Here, 59e13dbc3b27ee5090fd390f23e45a68 is the sys\_id of a maintenance plan record.

        **Note:** Workplace Maintenance managers should manually copy the sys\_id of a maintenance plan record. This is a required step to optimize cleaning activities on a floor in a building. The AI agents perform space optimization on the floor of a selected building.

    -   After manually copying the maintenance plan sys\_id, run the Optimize cleaning activities scheduled job. This schedule job triggers the agentic AI workflow for optimizing cleaning activities on a floor of a selected building. The space optimization for location is done in the UTC time zone.
    -   The **Case Aggregator AI Agent** fetches all open maintenance cases based on the maintenance plan Id. It fetches cases that are either in **Draft**, **Ready**, or **Awaiting Approval** state in the system for about 48 hours \(two days\).
-   **Utilization rate AI agent** takes a list of available maintenance cases and calculates the utilization rate for each case. The utilization rate calculator calculates the utilization threshold for a floor in a building. The utilization rate calculator calculates the space optimization. It considers the available reservations and visitor registration for a selected floor in a building.
-   \(Optional\) Workplace Maintenance Managers can navigate to the context menu in an instance and enter **sn\_aia\_execution\_plan.list** in the Filter search box to open the Execution Plans table. This table showcases workplace agentic AI workflow execution status. Review the maintenance cases that are executed by the Optimize cleaning activities agentic AI workflow.
    -   Select an optimized cleaning activity agentic workflow.
    -   Select the **Tools Execution** tab to review the execution tools and execution status.
    -   A tag is added to the maintenance case after it’s optimized for the first time.

        The tag is added as an identifier to showcase that a selected maintenance case is processed for space optimization. It isn’t picked up again by the agentic AI workflow for processing. When a case is updated and processed again, the sys\_id of existing tags and the case is not tagged again. The sys\_id of the tag is used to identify processed maintenance cases from the non-processed maintenance cases.

-   The **Case optimizer AI agent** analyzes cases grouped by location, schedule type, and date to optimize resource utilization. It confirms that maintenance cases stay within the defined utilization thresholds by creating new cases when the utilization rate is too high and deactivating underutilized cases.
    -   Retrieves the utilization thresholds.
    -   The **sn\_wsd\_maintenance.optmise\_cleaning\_min\_utilisation\_threshold** property analyzes the minimum space utilization threshold. The default value is 40. If the utilization for a workplace maintenance case is below this range, it’s deactivated. It’s deactivated when it meets all the deactivation criteria.

        **Note:** For example, if a floor has only 1 reservation for a day, then, only 10% of space is optimized for a selected floor. This range falls below the minimum threshold utilization range of 40. The maintenance case in this case is deactivated. The deactivation of a maintenance case also depends on the interval time of a scheduled job. For example, if the schedule job is scheduled to run daily, the maintenance cases that are showing low space optimization are removed or deactivated by the agentic AI workflow. However, if a scheduled job is scheduled to run on an hourly basis, all maintenance cases showing minimum threshold value are removed or deactivated except one. The system retains one underutilized maintenance case before deactivating all other maintenance cases that are scheduled to run on an hourly basis. When cases get deactivated, the status changes to **Closed complete** in the Workplace Maintenance cases table.

    -   The **sn\_wsd\_maintenance.optmise\_cleaning\_max\_utilisation\_threshold** property analyzes the maximum utilization threshold for a maintenance case. The default value is 80. If the utilization for a workplace maintenance plan case falls within this range or is higher than this range, a new maintenance case is added by the Optimize Cleaning Activities agentic AI workflow. A new case is added so that the optimized cleaning activities are handled using a single maintenance case. A new maintenance case can process it efficiently.

1.  [Optimize cleaning activities agentic workflow](optimize-cleaning-activities-agent.md)  
This team of workplace agents can find open maintenance cases and optimize it for workplace maintenance activities. These agents can optimize a maintenance case based on the utilization rate of a location for which a maintenance case is created.

**Parent Topic:**[Using AI agent workflows in Now Assist for WSD](now-assist-wsd-using-agentic-use-cases.md)

