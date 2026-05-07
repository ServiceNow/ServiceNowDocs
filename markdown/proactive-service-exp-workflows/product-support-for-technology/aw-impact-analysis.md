---
title: Resolve an incident record in Proactive Service Experience Workflows
description: Resolve an incident record by creating cases from record so that you can identify and solve network issues for your enterprise customers.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Identify affected accounts, Proactive Service Experience Workflow, Use, Product Support for Technology]
---

# Resolve an incident record in Proactive Service Experience Workflows

Resolve an incident record by creating cases from record so that you can identify and solve network issues for your enterprise customers.

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

6.  See the affected accounts by selecting the **Customer impact** tab.

    To learn more about the **Customer impact** tab, see [Enhancing customer impact visibility for PSEW processes](../concept/enhance-customer-impact-visibility-psew-process.md).

7.  Look for the names of the customers who are affected by selecting the Affected accounts section and checking the Account column.

    Typically, the network coordinator creates cases so that the impacted customers are proactively notified of the network-initiated issues.

8.  Generate proactive cases for the affected customers.

    To learn more see, [Generate a proactive case from the customer impact tab](generate-proactive-case-customer-impact-tab.md).

9.  Notify a customer about the creation of case record.

    To learn more, see [Communicate with customer about proactive case](create-communication-customer-impact-tab.md).

10. Update the case record about the resolution progress.

    To learn more, see [Update the proactive case with the resolution progress notes](notify-customer-proactive-case.md).

11. Create reactive case record.

    To learn more, see [Create a reactive case from the incident record](create-reactive-case-cutomer-impact-tab.md).

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

