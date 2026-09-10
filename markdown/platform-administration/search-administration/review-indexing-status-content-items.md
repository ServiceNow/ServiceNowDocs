---
title: Review indexing status for individual content items
description: View indexing status, selected fields, errors, and user and group access permissions for individual content items using the Index inspector tool in the external content connector editor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/review-indexing-status-content-items.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Review, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Review indexing status for individual content items

View indexing status, selected fields, errors, and user and group access permissions for individual content items using the Index inspector tool in the external content connector editor.

## Before you begin

Roles required: sn\_ext\_conn.xcc\_admin and ais\_high\_security\_admin

**Note:** The ais\_high\_security\_admin role is an elevated privilege role. To learn more about elevated privilege roles, see [Elevated privilege roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_ElevatedPrivilege.md). For details on the ais\_high\_security\_admin elevated privilege role, see [Assign roles to AI Search administrators and users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/assign-ais-admin-role.md).

## About this task

Use the index inspector tool to review individual content items retrieved by an external content connector. You can view an item's indexing status and see whether errors were encountered while retrieving and indexing it. View a content item's details to see its activity and selected fields, or to verify user access to the item in secure search.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You must be in this scope to create or edit external content connectors.

3.  In the Connectors list, select the record for the external content connector whose content items you want to view indexing status for.

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

\[Omitted image "elevate-role-polaris-ui.png"\] Alt text: User menu with Elevate role action highlighted in Next Experience UI.

</td></tr><tr><td>

Core UI

</td><td>

In the banner frame, select your name to open the user menu, then select **Elevate Roles**.\[Omitted image "adv-ais-tools-user-menu-before.png"\] Alt text: User menu with Elevate Roles action highlighted in Core UI.

</td></tr></tbody>
</table>        A dialog box appears, displaying a checklist of your available privileged roles.

        \[Omitted image "elevate-role-dialog-polaris-ui-ais.png"\] Alt text: Dialog box displaying privileged roles in Next Experience UI.

    2.  In the dialog box, select the **ais\_high\_security\_admin** option, then select **Update** \(in Next Experience UI\) or **OK**.

        The page reloads and an elevated role indicator appears next to your user name in the user menu. In Next Experience UI, this indicator displays the names of the active privileged roles. In Core UI, the indicator displays the elevated role icon \[Omitted image "icon-elevated-role-ui16.png"\] Alt text:.

        \[Omitted image "elevated-polaris-ui.png"\] Alt text: User menu showing elevated role indicator in Next Experience UI.

        **Note:** When the page reloads, any unsaved edits are lost.

5.  In the connector editor, select the Index inspector tab.

6.  In the **Before you access the index inspector** modal window, select the **I agree to the following disclaimer** option, then select **Access index inspector**.

7.  Enter the title, source system URL, or ID for a content item that you want to view indexing status for, then select **Search index** or press Enter.

    The system displays a list of content items that match your search. Each content item entry shows indicators for the item's indexing status and the number of errors encountered while retrieving and indexing it.

8.  To view additional details on a content item, select its **Open details** link.

    The system displays details on the item including its URL, ID, and selected fields. A **Who can see this document?** section shows users and groups with access to the item \(for secure search\). An **Activity** section reports the item's status from the most recent connector crawl and its last seen and last indexed timestamps. This section also displays entries for the most recent errors encountered while retrieving or indexing the item. You can select **See all** to view more error entries.

    **Note:** You can hide index fields so they're not displayed on documents in the index inspector. For details on hiding fields in the index inspector, see [Hide fields in the index inspector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/hide-fields-index-inspector.md).

9.  To verify whether a specific user can see the content item in search results, perform these steps.

    1.  In the **Who can see this document?** accessibility section, enter a user's email address into the **Test with user** field.

    2.  Select the Search icon \[Omitted image "index-inspector-access-search-icon.png"\] Alt text:.

        The system reports whether the specified user can view the content item in search results or not.


-   **[Hide fields in the index inspector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/hide-fields-index-inspector.md)**  
Suppress display of fields on documents in the index inspector.

**Parent Topic:**[Reviewing external content connector crawl results and analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/reviewing-external-content-connector-results-and-analytics.md)

