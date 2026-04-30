---
title: Set the Recommended Actions application system properties
description: Set the system properties for the Recommended Actions application to view the recommendations in the contextual panel of the Automation Center Workspace.
locale: en-US
release: yokohama
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring the Recommended Actions application with Automation Center, Configuring Automation Center, Automation Center, Data and Automation]
---

# Set the Recommended Actions application system properties

Set the system properties for the Recommended Actions application to view the recommendations in the contextual panel of the Automation Center Workspace.

## Before you begin

**Note:** In the recommendations list, only automations that are in Published and In-maintenance state are displayed and automation requests in all states except Publish state are displayed.

Role required: admin

## Procedure

1.  Set the system property, **sn\_ac.use\_recommended\_actions**, to **True**.


## Result

The Recommendations contextual panel is displayed in the Automation Center Workspace.

![Recommendations contextual panel](../images/reco-options.png "Recommendations contextual panel")

-   Recommendations will be displayed in the contextual panel of the automation request record.
-   Select **Dismiss** to remove the recommendation from the list.
-   Select **View details** to view the details of the recommendation.
-   If more than three applications are used for an automation request, then three are listed, and the rest are displayed as numbers. When you select **View details**, you can see all the applications used.
-   All other details of the recommended automations and automation requests, such as state, actual cost, and actual time are also displayed.

**Parent Topic:**[Configuring the Recommended Actions application with Automation Center](../concept/config-ra.md)

