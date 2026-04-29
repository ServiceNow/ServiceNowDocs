---
title: Add a dashboard to dashboard library
description: Add a dashboard to the Related Dashboards page in Assistant analytics so that users can access it from the dashboard library.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2026-02-17"
reading_time_minutes: 1
breadcrumb: [Related dashboards page, Analyzing assistants, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Add a dashboard to dashboard library

Add a dashboard to the Related Dashboards page in Assistant analytics so that users can access it from the dashboard library.

## Before you begin

Role required: virtual\_agent\_admin

1.  Ensure you have the dashboard created in Platform Analytics.
2.  Configure the dashboard visibility in Platform Analytics to include Assistant Designer. See [Configure Platform Analytics dashboard details](https://www.servicenow.com/docs/access?context=config-db-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) for more information.
3.  Share the dashboard with virtual\_agent-admin role. See [Share a Platform Analytics dashboard](https://www.servicenow.com/docs/access?context=share-db-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) for more information.

## About this task

Adding a dashboard to the library makes it available to users on the Related Dashboards page. You can specify metadata such as the display name, description, category to help users find and identify the dashboard.

## Procedure

1.  Navigate to **All** &gt; **Assistant Designer** &gt; **Analytics** and select Related Dashboards in the left navigation.

2.  Select **Add Dashboard** in the Dashboard Library.

    ![Add Dashboard modal in Dashboard Library](../image/NAinVA-assistant-designer-analytics-add-dashboard.png "Add Dashboard modal")

3.  On the **Add Dashboard** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the dashboard in Platform Analytics. Use the field to search for and select an existing dashboard to add to the library. This field is required.|
    |Display Name|Name that appears on the dashboard card in the library. Enter a name as per your requirements.|
    |Description \(Optional\)|Description of the dashboard you want to add to the library. Enter a brief description of the dashboard.|
    |Owner|Displays the owner of the selected dashboard. This field is read-only.|
    |Updated by|Displays the user who last updated the dashboard. This field is read-only.|
    |Updated on|Displays the date when the dashboard was last updated. This field is read-only.|
    |Pin dashboard|Select the check box to automatically pin the dashboard to the Pinned dashboards section after adding it to the library.|

4.  Select **Add** to add the dashboard to the library.

    The dashboard is added to All dashboards section. If you selected the Pin dashboard check box, the dashboard appears in the Pinned dashboards section as well.


