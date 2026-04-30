---
title: Related List configuration
description: You can add new related lists or new related list groups, and modify existing groups or related lists that appear in the Security Analyst Workspace.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Additional Security Analyst Workspace configuration, Configure the Security Analyst Workspace, Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Related List configuration

You can add new related lists or new related list groups, and modify existing groups or related lists that appear in the Security Analyst Workspace.

![Security Analyst Workspace: Related Lists](../image/sir-new-ui-setup-main-related.png)

**Add a Related List Group**

To add a Related List Group, follow these steps:

1.  Navigate to **Security Incidents** &gt; **Analyst Workspace Setup \(New UI\)** &gt; **Related List Configurations**.
2.  Click **New** to add a new Related List Group. Enter the Group Name and the Order in which it should be appear on the Incidents \(New UI\) page.
3.  Click **Submit**. The newly added group appears in the Related List Groups page.

    ![Security Analyst Workspace: New Related List](../image/cj-sir-new-ui-setup5.png)


**Add a Related List**

To add a new Related List, follow these steps:

1.  Click on a Related List Group link.
2.  In the Related Lists section, click **Add** to add a new related list.

    If you don't see the **Add** button, check if you are in same application scope as the Related List Group.

3.  Select the Related List to be included in the group.

    **Note:** If you do not see a specific related list, do the following:

    1.  Navigate to **System UI** &gt; **Related Lists** and search for Related Lists present in the `sn_si_incident` table.
    2.  Click on the `sn_si_incident` table associated with the **SIR New UI**view.
    3.  In the Related List Entries section, click **New** to add the Related List to the **SIR New UI** view.
4.  Specify the order in which it should appear and click **Submit**.

    The Related List that you have added will appear in the Security Analyst Workspace.


To modify an existing Related List Group, click the Group Name to navigate to the Related List Group page. You can modify the Group Name, Order, and add or delete Related Lists from the group.

