---
title: Diagnose search result access issues using the Search Preview UI
description: Use the Search Preview UI and the AI Search High Security administrator elevated privilege role to determine whether filters prevent a search user from viewing a specific search result in the AI Search index.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-13"
reading_time_minutes: 3
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer]
---

# Diagnose search result access issues using the Search Preview UI

Use the Search Preview UI and the AI Search High Security administrator elevated privilege role to determine whether filters prevent a search user from viewing a specific search result in the AI Search index.

## Before you begin

Role required: ais\_admin, ais\_high\_security\_admin, and impersonator.

## About this task

Use the Search Preview UI to diagnose filter configurations that prevent a search user from seeing a specific search result in the AI Search index. First, search as the affected user in the Search Preview UI to confirm that the search result in question isn't returned for them. Next, end impersonation and repeat the search after elevating to the ais\_high\_security\_admin role to bypass all search source and content security filters. If the desired search result appears in your elevated search, examine its search source and content security filter settings to determine why the affected user can't view it.

**Note:** Changing the value of the **Search as User** field in the Search Preview UI's User tool terminates elevated privileges for the ais\_high\_security\_admin role. To bypass filters after changing this field's value, you must re-elevate to the ais\_high\_security\_admin role, as directed in the following procedure.

## Procedure

1.  Navigate to **AI Search** &gt; **Preview** &gt; **Search Preview \(New\)**.

2.  Select the Search Preview UI's Profile tool ![](../image/search-preview-new-icon-user.png) and enter the affected user's name into the **Search as user** field.

    **Note:** For more details on the **Search as user** field, see [Search Preview admin tools](../reference/search-preview-ui-new-admin-tools.md).

3.  In the Preview types list, select **Full visual view**.

4.  In the Search mode list, select the mode used by the search application configuration for the portal or search application where the affected user is unable to see the search result in question.

5.  In the Search Application list, select the search application configuration for the portal or search application where the affected user is unable to see the search result in question.

6.  In the Card view list, select **Result cards with details**.

7.  Enter the search query of interest into the search input field and press Enter or select the Submit search icon ![](../image/search-preview-new-icon-submit-search.png) to search as the affected user.

    Search results appear, matching those seen by the affected user for the search query of interest in the selected portal or search application. Some results that match your search terms may be hidden by search source or content security filters.

8.  Elevate to the ais\_high\_security\_admin role:

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

9.  Repeat the search of interest without impersonating the affected user.

    Search results appear with no search source or content security filters applied.


## What to do next

Compare the two search result sets. If the search result in question appears only in the elevated search, a search source or content security filter prevents the affected user from viewing that result. If the search result doesn't appear in either search, it's not present in the AI Search index.

If the search result in question is indexed from an external document, you can debug the external content security access permission filter for the affected user to see whether it prevents access to the search result. For details on this procedure, see [Debug external content security filters for a ServiceNow AI Platform user](debug-ext-security-perms-user-ais.md).

**Parent Topic:**[Administering AI Search](../concept/administer-ais.md)

