---
title: View data on configuration items on the preview panel in Express List
description: View additional details about configuration items \(CIs\) that are bound to alerts on the Express List preview panel.
locale: en-US
release: yokohama
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View data on configuration items on the preview panel in Express List

View additional details about configuration items \(CIs\) that are bound to alerts on the Express List preview panel.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon: ![Express list icon](../../event-management/image/express-list1.png).

3.  In the Active alerts list, select an alert check box.

4.  On the preview panel, open the Info tab.

5.  Hover over the Configuration item section to display information icons.

    ![Configuration item on the preview panel Info tab.](../image/el-ci-info.png)

6.  Display extra information on a CI by selecting the relevant icon.

    |Icon|Name|Description|
    |----|----|-----------|
    |![Info icon.](../image/el-info-icon.png)|Info|Shows the class, IP address, location, and environment of the CI.|
    |![Contact person/group icon.](../image/el-contact-person-icon.png)|Contact person/group|Shows the name of the owner of the CI, the support group assigned to it, and avatars of the individual team members.|

7.  View how the current CI is connected to other CIs by selecting **View CI topology** in the additional information panel.

    The **Dependency View** map opens. The map visually represents the relationships between CIs, helping you understand how different components are interconnected.


