---
title: Case Management - Key features, Actions &amp; Case details
description: The Workplace Central Case management workspace is an all-in-one workspace using which a case manager can manage hundreds of workplace cases created in the organization.
locale: en-US
release: yokohama
product: Workplace Central
classification: workplace-central
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 14
breadcrumb: [Reference, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Case Management - Key features, Actions &amp; Case details

The Workplace Central Case management workspace is an all-in-one workspace using which a case manager can manage hundreds of workplace cases created in the organization.

## Case management - Key features

As a case manager, monitor the large number of workplace cases incoming daily at any time using the workspace. Check the number of active workplace cases, the cases that have breached SLA and those that are critical. The workspace enables you to focus on priority cases by providing you a categorized display. The workspace enables you to perform the following:

-   You can analyze the number of cases opened and closed on a weekly basis. You can know the monthly volume of cases based on the workplace services.
-   You can view the case details in an organized display where you can focus on the most important actions and details to help you resolve the case quickly. You can edit a case, update case details, view the details of the employee who has requested the case and also know the location specified in the case on a floor map.
-   As an admin or case admin, you can cancel a case if it’s no longer required. Similarly, as a move admin, you can cancel a move case and as a maintenance admin you can cancel a maintenance case.
-   In case of a move cases, you can view the 'From location' and 'To location' on the map. You can know the date by when the move must be implemented.
-   In case of a maintenance cases, you can view the details related to the asset specified and know the location of the asset specified on the map. You know the details such as the product model and asset-related details.
-   When there are hundreds of cases like regular workplace cases, move cases and, maintenance cases, you can sort and apply a filter on the cases to work on them based on priority.
-   You can export the list of cases if necessary.

The landing page of the workspace is categorized as follows:

-   **Overview**: The **Overview** section displays the metrics of the cases. You can view the number of cases under various categories and also view a graph of the volume of cases.
-   **All active cases**: The **All active cases** section displays a detailed list view of all the currently active cases including the normal workplace cases, move cases, and maintenance cases.

![Case management - Overview and All active cases sections.](../images/casemgmt-landingpage-withlabel.png)

## Case management - Metrics \(Overview\)

The workspace displays the metrics of all the workplace cases under the **Overview** section. The **Overview** section displays the following information:

-   **Metrics**

    The metrics section displays the following case numbers in cards:

    -   **All active cases**: Displays the number of active cases currently requested in the organization. The number includes the cases that are in Draft, and other statuses except Cancelled, Closed incomplete and Closed complete.
    -   **Open critical cases**: Displays the number of critical cases that are currently open.
    -   **SLAs breached**: Displays the total number of cases that have breached SLAs that is the cases that have crossed the deadline to be resolved.
    -   **Unassigned cases**: Displays the total number of unassigned cases.
    -   **Cases awaiting approval**: Displays the total number of cases that are awaiting to be approved.
    You can select the metric card to view a detailed list of the cases. The case numbers are displayed as WCASEXXXX for workplace cases, WMCXXXX for maintenance cases and WMOVEXXXX for move cases same as in the Workplace Case Management application. In the list view, you can perform the following actions:

    -   Refresh the list and edit the columns of the list.
    -   Sort the list base don how you want to view them.
    -   Copy the URL to the clipboard.
    -   Filter the list based on various conditions and view the filtered conditions in a side panel. You can also get an advanced view of these filters using the **Advanced view** option.
    -   Export the workplace cases into the desired format using the **Export** option.
    -   Create a workplace case using the **New** option. For more information, refer to [Create a workplace service case](../task/create-a-case-casemgmtworkspace.md). Instead of using the [Workplace Service Portal](../../workplace-service-delivery/concept/workplace-services-portal-wsd.md) to submit a workplace service request on behalf of an employee for any other reason, you can directly raise a request using the Case management workspace.
    -   Assign the case to a user using the **Assign** option.
    When you open the list view, the left panel displays a list view of the above metric cards. Additionally, the list view also enables you to view **All cases** and **All resolved cases**. You can also switch to the **My Lists** tab in the panel and create a custom list based on what other metrics you want to view using the **Add new list** option. For more information, refer to [Create your own list to view case metrics](../task/create-your-own-list-to-view-case-metrics.md).

    ![My Lists tab.](../images/casemgmt-mylist.png)

-   **Graphs**

    The workspace also displays a graph with the volume of cases based on workplace services. You can also apply additional filters based on how you want to view them. By default, the graphs are displayed with the filter set as **Workplace Service** only. The page displays the following graphs:

    -   **Opened Vs Closed cases in last 30 days**: Displays the total number of cases opened and closed in the past 30 days in a week-based view. You can select the graph to view the details of the cases.
    -   **Volume of cases by workplace service**: Displays the total volume of cases based on workplace services from the past six months \(including the current month\). You can select the graph to view the cases associated with the selected workplace service.

## Case management - List view

You can view a detailed list of all the workplace cases currently active in the application in the **All active cases** section. The list view displays the cases as WCASEXXXX for normal workplace cases, WMCXXXX for maintenance cases and WMOVEXXXX for move cases. You can view the following details in the list view:

-   The workplace case number
-   The workplace service using which the case was requested
-   A short description about the case
-   Priority of the case
-   Employee for whom the case is requested for
-   Date when the case was requested

On the list, you can perform the following actions:

-   Refresh the list.
-   Edit the columns of the list based on what information that you want to view.
-   Apply filter conditions on the list and also change whenever needed.
-   Assign a single or multiple cases to another user using the **Assign** option.
-   Export the cases to the desired format using the **Export** option.
-   Create a workplace service case at any time using the **New** option. Instead of using the [Workplace Service Portal](../../workplace-service-delivery/concept/workplace-services-portal-wsd.md) to submit a workplace service request on behalf of an employee for any other reason, you can directly raise a request using the Case management workspace.

## Case details page

When you select a case to view its details, the case details are displayed in a separate tab. The case details page displays the details in an organized format and in various sections.

![Case management - Case details page.](../images/casemgmt-casedetails.png)

The case details are categorized in the following views:

-   **\(1\) Form-based view**

    When you open a case, the basic details of the case such as the case **Number**, **Requested for**, **Opened by** and current **State** of the case are displayed on the header. The details of the case are displayed in a form-based view same as displayed in the Workplace Case Management application. The form enables you to view the following information related to the case:

    -   **Details**

        By default, the page displays the information under the **Details** tab. The **Details** tab displays the workplace case information entered by the requestor. All the form fields with the details are displayed.

        -   You can view details such as the **Workplace service** using which the case was requested, the **Workplace location**, **Assignment group**, **Assigned to** user, detailed **Description**, **Items at the location** and more.
        -   For move cases, you can also view the details such as **From location**, **To location**, **Reason** for move.
        -   For maintenance cases, you can also view the details such as the **Product model**, **Enterprise asset**.
        In the **Details** view, you can add comments in the **Compose** panel and post it on the case. You can also add private work notes.

        The panel also displays all the activities performed on the case in the **Activity** section of the panel.

    -   **Child cases**

        The **Child cases** displays the child cases created with the workplace case. You can view details of the child cases such as the **Number**, **Short description**, **State**, **Assigned to** user, **Workplace task type**, **Workplace location** and more. You can edit the columns, refresh the list and apply filters on the cases.

        You can also create a child case if necessary using the **New** option. To create a child case, refer to [Create a child case and a child task](../task/create-a-child-case-and-a-child-task-casemgmtworkspace.md).

    -   **Child tasks**

        The **Child tasks** displays the child tasks created with the workplace case. You can view details of the child task such as the **Number**, **Short description**, **State**, **Assigned to** user, **Workplace task type**, **Workplace location** and more. You can edit the columns, refresh the list and apply filters on the tasks.

        You can also create a child task if necessary using the **New** option. To create a child task, refer to [Create a child case and a child task](../task/create-a-child-case-and-a-child-task-casemgmtworkspace.md).

    -   **Approvers**

        The **Approvers** displays the approvers of the case.

    -   **Case SLAs**

        The **Case SLA\(s\)** displays the SLAs associated with the case. You can view the SLA definitions defined for the cases associated with the case. You can also add an SLA using the **New** option.

    -   **Attached Knowledge**

        The **Attached knowledge** displays the attached knowledge articles with the case. You can add a knowledge article using the **New** option.

    -   **KB Articles Read by User**

        Displays the knowledge base articles read by the user associated with the case.

    -   **Related cases**

        The **Related cases** displays the cases that are related with the case. You can also create a case using the **New** option.

    -   **Workplace cases**

        The **Workplace cases** tab appears when you open a maintenance case. You can view the workplace cases associated with the maintenance case. You can create a case using the **New** option.

    -   **Requested Service Items**

        The **Requested Service Items** displays the workplace service items that are requested with the case.

-   **\(2\) Action panel**

    The details page displays a side panel on the right side that enables you to perform various actions and also view important details to help you resolve the case. The side panel consists of the following options:

    -   **At a glance**: When you open the case, by default, the page displays the **Requested for** employee details if available in the **Employee details** panel. This panel appears when the At a Glance \(![At a glance icon.](../images/casemgmt-ataglanceicon.png)\) option is selected. The details include the name of the employee, the email address of the employee using which you can send an email directly to the employee and the contact details. If the employee details are unavailable, then the admin or the case manager details are displayed.
    -   **Knowledge Articles**: Select the Knowledge Article icon \(![Knowledge Article icon.](../images/casemgmt-knowledgeicon.png)\) to view knowledge articles based on the case. You can **Flag** the article, view the article in a separate tab using the **Full view** option and mark the article as useful using the **Helpful** option.
    -   **Attachment**: Select Attachment icon \(![Attachment icon.](../images/casemgmt-attachementicon.png)\) to view the attachments in the case. You can also upload attachments if necessary.
    -   **Template**: Select the Template icon \(![Template icon.](../images/casemgmt-templateicon.png)\) to view the templates associated with the case. If you selected your own template, you can view them in the **My Template** tab. You can also create a template using the Create template option \(![Create template icon.](../images/casemgmt-createtempicon.png)\).
    -   **Location**: Select the Location icon \(![Location icon.](../images/casemgmt-locationicon.png)\) to view the workplace location specified in the case. The **Workplace Location** panel displays the details of the location such as the **Floor**,**Building**, **Campus** and **Region**. The location is also displayed on a floor map. You can drag on the map and also zoom in/out for a better view.
        -   For a move case, the **Location** panel displays the details of the **From location** and **To location** under the **Move from** and **Move to** tabs.
        -   For a maintenance case, the **Workplace location** panel displays the location of the asset specified in the case. If an asset isn’t specified, then the workplace location selected in the case is specified.
    -   **Fulfilment instructions**: Select the Fulfillment instructions icon \(![Fulfilment instructions icon.](../images/casemgmt-fulfimenticon.png)\) to view the fulfillment instructions related to the case.
    -   **Checklist**: Select the Checklist icon \(![Checklist icon.](../images/casemgmt-checklisticon.png)\) to view the checklist of the case. You can mark the checklist if it’s done and also add checklist items using the **Edit** option.

You can perform the following actions on a case at any time:

-   **Cancel**

    Cancel a case at any time if it’s no longer required. Cancelling the case will cancel all the child cases and tasks associated with it. The state of the cases and tasks is set as Cancelled.

-   **Save**

    Save the changes that you made on the case using the **Save** option.

-   **Delete**

    As an admin, delete a case record completely from the application.

    **Important:** Only an admin can delete a case. A case admin can delete only a workplace case, a move admin can delete only a move case and a maintenance admin can delete only a maintenance case.


**Parent Topic:**[Workplace Central reference](../concept/workplace-central-references.md)

**Related topics**  


[Components installed with Workplace Central](components-installed-with-workplace-central.md)

[Space Optimization - Key features and actions](space-optmization-features-and-actions-.md)

[Workplace Central Event planner](event-planner-key-features-actions-views.md)

[Scenario and Building - Views, states, settings, and key features](scenario-planning-views-actions-keyfeatures-.md)

[Space request approvals, states, actions, and key features](space-request-states-and-view.md)

[Move management key features and actions](move-mgmt-views-states-actions.md)

[Schedule Plan details form](schedule-plan-details-form.md)

[Scenario details form](scenario-details-form.md)

[Space Deployment Plan](space-deployment-plan.md)

[User Deployment Plan](user-deployment-plan.md)

[Excel column lengths for move projects](move-excel-char-limit.md)

[Move conflicts for projects created via Excel upload](excel-upload-conflicts.md)

[Workplace Central troubleshooting](workplace-central-troubleshooting.md)

