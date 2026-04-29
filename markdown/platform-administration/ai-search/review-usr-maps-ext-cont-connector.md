---
title: Review user permissions for an external content connector
description: View user and group access permissions retrieved by an external content connector, and see how the connector maps those permissions to your ServiceNow AI Platform instance's users.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Review, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Review user permissions for an external content connector

View user and group access permissions retrieved by an external content connector, and see how the connector maps those permissions to your ServiceNow AI Platform® instance's users.

## Before you begin

Role required: ais\_admin, plus ais\_high\_security\_admin to view full user permission details

## About this task

The User permissions list for an external content connector shows user and group access permissions retrieved from the connector's source system, along with details of how those permissions are mapped to your ServiceNow AI Platform instance's users. Review this information when you want to verify user and group permission mappings for your external content connector.

To view the user permissions list, you must elevate to the ais\_high\_security\_admin role. If you don't elevate or don't have this role, you can see the number of user permissions created for the external content connector, but can't see details of those user permissions.

**Note:** The following external content connectors don't retrieve user or group access permissions. You can't run user permission crawls for these connectors.

-   Adobe Experience Manager as a Cloud Service external content connector
-   Amazon S3 external content connector
-   Cornerstone external content connector
-   ServiceNow® product documentation external content connector
-   Slack external content connector
-   Trello external content connector
-   Webcrawler external content connector

The Atlassian Confluence Cloud external content connector only retrieves permissions for Confluence Cloud users who have made their email addresses visible to all users. To allow user permission, each Confluence Cloud user must set their own email visibility to **Anyone** as explained in the [https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/](https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/) Atlassian support resource.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors pane, select the record for the external content connector whose user permissions you want to review.

3.  In the connector editor, select the **User permissions** tab.

    The User permissions page shows the total count of user permissions created by the external content connector.

4.  Elevate to the ais\_high\_security\_admin role:

    1.  Perform the appropriate action for your version of the UI:

<table id="table_els_wyl_vpb"><thead><tr><th>

UI version

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Next Experience UI

</td><td>

In the banner frame, select the icon for your account to open the user menu, then select **Elevate role**.

![User menu with Elevate role action highlighted in Next Experience UI.](../image/elevate-role-polaris-ui.png)

</td></tr><tr><td>

Core UI

</td><td>

In the banner frame, select your name to open the user menu, then select **Elevate Roles**.![User menu with Elevate Roles action highlighted in Core UI.](../../../use/dashboards/image/adv-ais-tools-user-menu-before.png)

</td></tr></tbody>
</table>        A dialog box appears, displaying a checklist of your available privileged roles.

        ![Dialog box displaying privileged roles in Next Experience UI.](../image/elevate-role-dialog-polaris-ui-ais.png)

    2.  In the dialog box, select the **ais\_high\_security\_admin** option, then select **Update** \(in Next Experience UI\) or **OK**.

        The page reloads and an elevated role indicator appears next to your user name in the user menu. In Next Experience UI, this indicator displays the names of the active privileged roles. In Core UI, the indicator displays the elevated role icon ![](../../security/image/icon-elevated-role-ui16.png).

        ![User menu showing elevated role indicator in Next Experience UI.](../image/elevated-polaris-ui.png)

        **Note:** When the page reloads, any unsaved edits are lost.

5.  Review the entries in the User permissions list.

    Each entry shows a single ServiceNow AI Platform user along with the external user mapped to them and any external group memberships associated with that external user. You can sort and filter the list to locate entries of interest.


**Parent Topic:**[Reviewing external content connector crawl results and analytics](../concept/reviewing-external-content-connector-results-and-analytics.md)

