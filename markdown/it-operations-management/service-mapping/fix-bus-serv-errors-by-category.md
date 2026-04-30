---
title: Fix application service errors in bulk
description: Service Mapping classifies errors by their root cause, for example, missing credentials or task timeout. For a fast and efficient process, fix errors belonging to the same category in bulk.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Fix application service errors in bulk

Service Mapping classifies errors by their root cause, for example, missing credentials or task timeout. For a fast and efficient process, fix errors belonging to the same category in bulk.

## Before you begin

Role required: service\_mapping\_admin or admin

## About this task

You can view errors by category, for example, **Configuration**, **Network**, and **Credentials**. Each category tile also displays the error counter.

As part of the Service Mapping workflow, after you map application services in bulk, you can fix multiple application service errors in bulk \(as a group\).

![Fixing errors in bulk as part of the Service Mapping workflow](../image/SMMapFlowFixBulk.png "Fixing errors in bulk workflow")

After performing initial mapping, Service Mapping rediscovers configuration items \(CIs\) regularly, constantly updating the list of errors. Discovery schedules define how often Service Mapping runs the discovery process for CIs. Service Mapping discovers only CIs belonging to application services with Operational status.

There may be discovery errors not assigned to any category:

-   After upgrading Service Mapping from Jakarta release or earlier.
-   If there are configuration items \(CIs\) that have errors associated with them, and that were first removed from application services and then readded to application services.

## Procedure

1.  Navigate to **All** &gt; **Service Mapping** &gt; **Home** and then click **Fix Your Services** in the **Fix** box.

    The number in the **Fix** box indicates the number of affected service maps. Click **Update** \(![The Update button](../image/update-button.png)\) to update the display.

    **Note:** To [fix the errors for a particular service](fix-or-ignore-errors-business-service-map.md) instead, click **Manage Errors by Service**.

2.  If there are uncategorized errors, you can categorize them by service instance:

    1.  Click **View Uncategorized Errors by Service**.

    2.  Click the relevant service name.

    3.  On the service instance map, click **Run Discovery**.

        Service Mapping discovers all CIs discovered with errors and belonging to this service instance.

3.  If there are uncategorized errors, categorize them by clicking **Rediscover Relevant CIs**, and clicking **Continue** in the confirmation message.

    Service Mapping discovers all CIs discovered with errors and belonging to application services with Operational status.

4.  Click an error category box.

    In the example below, configuration errors are selected.

    -   The Errors by Category page organizes errors by high, medium, and low impact on the services.
    -   For each impact category, errors are grouped into boxes by error code \(possibly the root cause\).
    -   If error tasks have been assigned, the task numbers appear in the box. Click a task to view details. Point to a task to view comments that the assigner might have added. A check mark indicates that a task is completed.
    ![Errors that share identical error codes](../image/error-code-box.png)

5.  To view the list of errors that share an error code, click the box.

    You can perform one of the **Recommended Actions** on items that you select or on all items in the list.

    In the example, **All patterns failed** is selected.

    ![Review the suggested actions under Recommended Actions.](../image/error-list.png)

6.  Click an action in the **Action on All** section, or select errors and click an action in the **Action on Selected** section.

    -   **Retry Discovery**

        Performs the full Discovery process. You typically perform Discovery after following the fix instructions that appear when you click **View instructions**.

    -   **View affected services**

        Displays a popup list of all services that are affected by the selected error. In the list, click a service to view service details.

    -   **Mark as assigned**

        Apply the **Mark as assigned** action when you plan to perform an out-of-band action to notify a person to fix the error \(typically a person who does not use the ServiceNow instance\). You can enter a **Comment** in the **Mark as Assigned** popup. Click **Update** to set the **Error Status** field in the error record as **Assigned** and associate the **Comment** with the error. To view the comment, point to the **Assigned** link.

        **Note:** The **Create ServiceNow task** action also sets the **Error Status** field in the error record as **Assigned**.

    -   **Create a ServiceNow task**

        Opens the ServiceNow Error task form in a pop-up window so you can create and assign a task for the selected errors. Sets the **Error Status** field in the error record as **Assigned**. For information on creating error tasks, see [Create a table](https://www.servicenow.com/docs/access?context=t_CreateATable&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [Create a task from an incident, problem, or change request](https://www.servicenow.com/docs/access?context=t_CreateTaskIntPrblmChange&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US).

        **Note:** The **Mark as assigned** action also sets the **Error Status** field in the error record as **Assigned**.

        ![Error task form](../image/error-task-popup.png)

    -   **Retry Discovery**

        Performs the full Discovery process. You typically perform Discovery after following the fix instructions that appear when you click **View instructions**.

    -   **View instructions**

        Displays a troubleshooting procedure in a pop-up window. Follow the steps to try to resolve the error.

    -   **Ignore Error**

        Right-click an error and then select **Ignore Error** to set the **Ignored** value to **true**.

    The system performs the action on the items, displays **In progress**, and then displays the result \(success or failure\) of the action. If the error is resolved, the **Error Status** field in the error record is set to **Resolved**.

    **Note:** If an action \(for example, Discovery\) is in progress, but taking too long, you can click **Stop** to stop the action.

7.  Click **Done** to close the status message.

8.  If you performed an action on a selection and the error was resolved, you can click **Resolve All** to apply the same action to all items in the list.


**Parent Topic:**[Application service mapping using classic Service Mapping](../concept/c_DefineMapBusinessServices.md)

**Related topics**  


[Map multiple application services suggested by classic Service Mapping](map-business-services-in-bulk.md)

[Map application services using tags with classic Service Mapping](map-service-tag.md)

[Map multiple application services from a CSV file using classic Service Mapping](import-business-services-csv.md)

[Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md)

[Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md)

[Review and approval of application service maps](business-service-approval.md)

[Fine-tune application services to implement owner requests](review-implement-business-service-maps.md)

[Application service completion](../concept/advanced-business-service-definitions.md)

[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

