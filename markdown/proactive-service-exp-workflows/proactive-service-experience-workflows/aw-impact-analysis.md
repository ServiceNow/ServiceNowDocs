---
title: Create cases from an incident record in Proactive Service Experience Workflows
description: Create cases from records so that you can identify and solve network issues for your enterprise customers.
locale: en-US
release: zurich
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Identify affected accounts, Use, Proactive Service Experience Workflows]
---

# Create cases from an incident record in Proactive Service Experience Workflows

Create cases from records so that you can identify and solve network issues for your enterprise customers.

## Before you begin

This task assumes that a workflow has already been triggered and an assignment group has been assigned.

Role required: sn\_ind\_tsm\_sdwan.PSEW\_USER

## About this task

After a workflow in Proactive Service Experience Workflows triggers, you can identify the customers and systems that are affected by the network issue. You can then either automatically create the individual cases for the impacted customers or create a major case and child cases for a larger number of affected customers.

## Procedure

1.  Navigate to the Service Operations Workspace, and select **List** &gt; **Incidents** &gt; **Open**.

2.  Select an incident from the list.

3.  In an existing incident, assign the incident.

4.  See the affected configuration items \(CIs\) by selecting the **Affected CIs** card.

5.  See the impacted services by selecting the **Impacted Services/CIs** card and selecting **Refresh Impacted Services**.

6.  See the affected accounts by selecting the **Affected Accounts** card and selecting **Identify Affected Accounts**.

    The ServiceNow® instance initiates an action to refresh the impacted services and to find the affected accounts.

7.  Look for the names of the customers who are affected by selecting the **Affected Accounts** card and checking the Name column.

    Typically, the network coordinator creates cases so that the impacted customers are proactively notified of the network-initiated issues.

8.  Generate proactive cases for the affected customers by selecting the Cases card and selecting **Generate Proactive Cases**.

    -   If the number of affected accounts is less than the threshold, then this action creates one case for each affected account. Otherwise, this action first creates a major case and then creates child cases \(one case for each affected account\).
    -   If you want to change the threshold, contact your administrator to change the value of the **sn\_ind\_tsm\_core.major\_case-affected\_account\_threshold** system property.
    -   In the **Cases** tab, the major case is indicated by **\[empty\]** in the Account and Contact columns. Cases where that information is populated are child cases of that major case.
9.  Create an ad-hoc case by selecting a case from the list and selecting **New**.

10. Notify a customer by selecting a case and selecting **Notify Customers**.

11. In the Notify Customers pop-up window, enter a descriptive note, and select **Notify**.

    A note is automatically inserted in the **Activity** field of the incident record and also in the selected cases record. If your customer updates the case with any message, it automatically synchronizes with the Incident record too.

    **Note:** By default, the Notify Customers functionality isn’t active. As an admin, you must set the property value **proactive\_workflows\_for\_providers.additional\_comments\_sync** to TRUE. Turn off the BR \(business rule\) **Update case worknote for comments change** to enable this functionality.

12. If you want to update the probable cause of the incident, select the **Cause** tab and save your message.

13. Resolve an incident by selecting **Resolve** on the incident record.

    In the Resolve pop-up window, enter the resolution code and resolution notes and select **Resolve**.

    **Note:** Only minor cases are automatically closed. For major cases, you must manually close all the related cases.


## Result

When the incident is resolved, it triggers the auto-closure of related cases.

-   If there’s no major case, all the related individual cases are resolved and are updated with the work notes. The following field values from the parent incident record are also populated in the related cases:
    -   Resolution Notes
    -   Resolution Code
    -   Probable Cause
-   If there’s a major case, the related cases don't get auto-resolved and a message is added to the work notes of the incident record, "There is a major case associated with this incident."The following field values from the parent incident record are populated in all the related major and child cases:
    -   Resolution Notes
    -   Resolution Code
    -   Probable Cause

**Parent Topic:**[About identifying affected accounts with Proactive Service Experience Workflows in Incident Management](../concept/psew-identify-act-incident.md)

