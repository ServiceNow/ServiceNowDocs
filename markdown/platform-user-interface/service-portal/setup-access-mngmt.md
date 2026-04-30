---
title: Set up Access Management Automation
description: Set up the Access Management Automation application by configuring the Service Portal page to use the default catalog items.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Access Management Automation, Configure a catalog in Service Portal, Create a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Set up Access Management Automation

Set up the Access Management Automation application by configuring the Service Portal page to use the default catalog items.

## Before you begin

-   This application requires an Integration Hub or Automation Engine subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).
-   Activate and configure one of the required spokes.

    -   Okta spoke
    -   Microsoft Entra ID spoke \(formerly Microsoft Entra ID spoke\)
    -   Microsoft Active Directory spoke
    **Note:** Configure only the required spokes. For example, if you want to manage access in Okta, configure the Okta spoke.

-   Activate the Access Management Automation app
-   Role required: admin

## Procedure

1.  Configure the decision tables to perform these tasks:

    -   Assign users, groups, or both to approve requested items.
    -   Assign users, groups, or both to take action on catalog tasks and incidents.
    -   Trigger subflow\(s\) if the automation fails.
    The flows in this application use decision tables to enable admins to configure approvers, assignments, and subflow routing without modifying any of the flows in Workflow Studio. In each decision table by default, you can modify the decision record to select an option \(group, user, or subflow\) that applies to all catalog items in the application. If you want to have different assignments, approvers, or subflows per catalog item, you can add new decisions for each catalog item within the decision tables.

    1.  Navigate to **System Definition** &gt; **Decision Tables**.

    2.  Open the required Access Management Automation decision table record.

        These steps should be repeated for each decision table.

    3.  Click the **Decisions** tab.

    4.  Click the decision record.

        ![Decision record.](../image/decision.png)

    5.  Select the required group, user, or subflow in **Answer**, depending on what the decision table is used for.

        ![Select the required Answer.](../image/condition.png)

        **Note:** Configure these seven decision tables and assign **Answer** as per your requirements.

        -   Access Mgmt. Catalog Task Group Assignment Policy
        -   Access Mgmt. Catalog Task User Assignment Policy
        -   Access Mgmt. Failed Automation Flow Policy
        -   Access Mgmt. Incident Group Assignment Policy
        -   Access Mgmt. Incident User Assignment Policy
        -   Access Mgmt. Requested Item Group Approval Policy
        -   Access Mgmt. Requested Item User Approval Policy
        If select the Create Incident subflow in the Access Mgmt. Failed Automation Flow Policy decision table, you should configure the incident assignment decision tables. If you choose the Create Event subflow, you can ignore the incident assignment decision tables.

2.  Configure the Service Portal page.

    **Note:** Ensure that you select **Default \[Global\]** and **Global** for current update set and application.

    ![Select the global value.](../image/global.png)

    1.  Navigate to **Service Portal** &gt; **Portals**.

    2.  Open the **Service Portal** record.

    3.  Click the **Catalogs** tab.

    4.  Click **Edit**.

    5.  Add **Access Management** to the **Service Portal** list.

        ![Add Access Management.](../image/access-management.png)

    6.  Click **Save**.


## What to do next

-   To view the catalog items, navigate to **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Catalogs** and click **Access Management**.
-   To request a catalog item:

    **Note:** User must have the sn\_acc\_mgmt\_sc.access\_mgmt\_user, ITIL, and Catalog Admin roles to create and submit catalog items.

    1.  Navigate to the Service Portal.
    2.  Click the **Catalog** tab.
    3.  Click **Browse by Categories**.
    4.  Select **Access Management**.![Access Management catalogs.](../image/access-management-catalogs.png)
    5.  Select the required service from the displayed categories.![Access Management category.](../image/categories.png)
    6.  Select the required action and submit the catalog item. When the request is approved, the associated flow is triggered and the required user can provide the approval. Activities are logged in the catalog item.
-   If you are using the application to manage access in Okta, ensure that the user has the Okta admin role to retrieve data in the Okta groups module. Also, the user must have the Okta admin role to submit request using the catalog item.
-   For information about customizing the widget and macro, see the KB article, [Access Management Automation - Widget &amp; Macro Customisations](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0993763).

**Parent Topic:**[Access Management Automation](../concept/access-management.md)

