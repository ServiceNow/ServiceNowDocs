---
title: Activate teams and services in SRM
description: Activate teams and services to be managed in the Service Reliability Management \(SRM\) application.
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Activate teams and services in SRM

Activate teams and services to be managed in the Service Reliability Management \(SRM\) application.

## Before you begin

Role required: srm\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Configurations**.

2.  Select **Service Reliability Management** &gt; **Activate** &gt; **Teams and services**.

3.  Select **Activate teams and services** to begin importing or adding teams.

4.  Use the condition builder to filter the teams shown in the Assignment groups list.

    **Note:**

    Filters on the same field use AND logic, and filters on different fields use OR logic. For example, filtering for multiple `Business Criticality` levels and `State = Open`, evaluates as `(Criticality = 1 OR 2 OR 3 OR 4) AND (State = Open)`.

    List view filters are saved automatically and persist when you navigate away and return.

5.  In the Assignment groups list, select the teams you want to add and then select **Activate**.

    You reach the **Activate services** option to add services.

6.  From the **Select a service class** list, select a service.

    The following service types are available:

    -   Application Services
    -   Mapped Application Services
    -   Calculated Application Services
    -   Dynamic CI Group
    -   Technical Services
    -   Tag-based Services
7.  Use the condition builder to add new services to the list view.

8.  Select the services that you want to add and then select **Activate**.

    The **Activate Services** pop-up opens.

9.  From the **Support Group** drop-down, select the relevant support group and select **Confirm**.


## Result

On the **Activate teams and services** page, the following options appear:

-   Existing teams
-   Existing services

You can select the options to view the teams or services.

**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Related topics**  


[Install Service Reliability Management from Admin Center or ServiceNow Store](sr-install-sr-store-app.md)

[Assign an administrator to Service Reliability Management](sr-assign-admins.md)

[Customize service approval settings in SRM](sr-add-approval-services.md)

[Customize team approval settings in SRM](sr-add-approval-teams.md)

[Configure error budget actions for breached SRM SLOs](sr-configure-error-budget.md)

[Approve a change request for SRM](sr-approve-change-req.md)

[Configure fields for escalation triggers](srm-configure-trigger-fields.md)

[Configure Twilio to send notifications in SRM](sr-add-twilio-key.md)

[Install the Alert Automation application](sr-install-aa-store-app.md)

