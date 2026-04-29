---
title: Create a case from a change request
description: Create a case from a change request in Proactive Service Experience Workflows so that you can notify your customers about a service outage and its resolution after the change implementation is complete.
locale: en-US
release: australia
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Proactive Service Experience Workflow, Use, Product Support for Technology]
---

# Create a case from a change request

Create a case from a change request in Proactive Service Experience Workflows so that you can notify your customers about a service outage and its resolution after the change implementation is complete.

## Before you begin

A change in workflow has been triggered. An assignment group with the planned start and end dates have already been set.

Role required: admin

## About this task

After a change in workflow Proactive Service Experience Workflows is triggered, you can identify the customers and systems that are affected by the change request. You can then either automatically create the individual cases for the impacted customers or notify your customers about the outages.

## Procedure

1.  In Service Operations Workspace, navigate to **List** &gt; **Changes** &gt; **Open** and select a change record.

2.  In an existing change record, assign the change request to a support engineer.

3.  Expand the Scope and impact section and select the **Affected CIs** card.

4.  See which services are impacted by selecting the **Impacted Services/CIs** card and then selecting **Refresh Impacted Services**.

    The instance initiates an action to refresh the impacted services and to find the affected accounts.

5.  See the list of outages by selecting the **Outages** card.

6.  See which accounts are affected in the Customer impact tab.

7.  See which consumers have been affected in the Customer impact tab.

8.  In the Details section, change the state of the Change record to **Authorize**.

    The cases for the affected customers are automatically created.

9.  When the change manager authorizes the change record and the status changes to **Scheduled**, you can update the state by selecting **Implement**, selecting **Review**, and then saving the record.

10. Select the resolution code from the drop-down list, enter the resolution notes before closing the change request, and update the state by selecting **Close**.


**Parent Topic:**[Using Proactive Service Experience Workflows](../concept/use-assurance-workflows.md)

**Related topics**  


[About identifying affected accounts with Proactive Service Experience Workflows in Incident Management](../concept/psew-identify-act-incident.md)

