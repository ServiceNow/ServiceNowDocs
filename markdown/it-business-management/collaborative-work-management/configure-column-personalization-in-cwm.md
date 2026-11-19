---
title: Configure columns available for personalization in CWM
description: Configure which columns are available in the column personalization panel in CWM by updating the default list layout for the relevant table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/collaborative-work-management/configure-column-personalization-in-cwm.html
release: zurich
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 1
breadcrumb: [Configure, Collaborative Work Management, Strategic Portfolio Management]
---

# Configure columns available for personalization in CWM

Configure which columns are available in the column personalization panel in CWM by updating the default list layout for the relevant table.

## Before you begin

Role required: admin

## About this task

CWM displays columns from the default list view of a table as available options in the column personalization panel. For stories, CWM uses the CWM view of the list instead of the default view.

## Procedure

1.  Navigate to the list view of the table you want to configure.

    For example, navigate to `incident.list` for the Incident table, `sn_cwm_task.list` for CWM tasks, or `rm_story.list` for stories.

2.  Right-click any row in the list to open the row context menu, and select **View** &gt; **Default view**.

    For stories \(`rm_story`\), select **View** &gt; **CWM view** instead.

    This step ensures you're configuring the list layout that CWM references for column personalization.

3.  Select the header of any column, and from the column menu select **Configure** &gt; **List Layout**.

4.  Add or remove the columns you want to make available for personalization, and save your changes.


## Result

Users can now select the updated columns when personalizing the display of CWM Boards. For more information, see [Personalize List, Gantt and Kanban display for CWM Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/personalize-cwm-board-views.md).

**Related topics**  


[Configure the list layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_ConfigureTheListLayout.md)

[Personalize List, Gantt and Kanban display for CWM Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/personalize-cwm-board-views.md)

