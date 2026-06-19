---
title: Configure language groups
description: After setting up individual language providers, you can define one or more language groups. Configuring language groups is an optional way to streamline the creation of translation requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/localization-workspace/lw-configure-language-groups.html
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [Language setup in Localization Workspace, Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure language groups

After setting up individual language providers, you can define one or more language groups. Configuring language groups is an optional way to streamline the creation of translation requests.

## Before you begin

-   Configure all individual language providers. The localization\_admin role is required to create a language provider. See [Configure a language provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/lw-configure-translation-provider.md).
-   Role required: sn\_lw.user. The sn\_lw.user role can create a language group by selecting from existing language providers.

## About this task

From version 2.0.2: When your users create translation requests, they can select configured language groups rather than adding each language individually to the request.

Individual languages may be included in more than one language group. If a language is included multiple times in one translation request, Localization Workspace clears out the preconfigured value for translation service provider. Then the translation requester must manually select the desired translation service provider.

**Note:** From version 3.0.0, a Guided Tour is available to assist localization admins and localization requesters \(localization\_admin and localization\_requestor\) with the setup of a language group. Access the guided tour by selecting the Help Center icon \[Omitted image "Banner\_HelpIcon.png"\] on the [Home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/lw-status-synchronization.md) screen.

## Procedure

1.  Navigate to **All** &gt; **Localization Workspace** &gt; **Language setup**, then select the **Language Groups** tab.

    \[Omitted image "lw-configure-language-group-grouped-list.png"\] Alt text: The Language setup area of Localization Workspace, with the Language Groups tab selected. Three groups have been configured.

2.  Select the **New** button to open the **Language Groups** modal window.

3.  In the modal window, enter a name for your group and an optional description.

4.  Select a Target language and its Translation provider.

    \[Omitted image "lw-configure-language-groups-dropdown.png"\] Alt text: The Language Groups modal window with an available language selected in the drop-down menu.

5.  Select the **Add new language** icon \[Omitted image "plus-outline-24.svg"\]to add another row.

    Language groups must have a minimum of at least two members.\[Omitted image "lw-configure-language-groups-add-new-lang.png"\] Alt text: The Language Groups modal window, with the Add new language icon highlighted. There are two languages in the example language group.

6.  Select **Submit** when you have finished adding all rows you want to include in the group.

7.  You can export the list of language groups into your choice of file formats \(Excel, CSV, JSON, PDF\) by selecting **Export** on the list view of Language Groups.

    The exported list can either be downloaded as a file or attached to an email. Select **Delivery Type** in the Export modal window to switch from file download \(default\) to the email attachment option.


## What to do next

You can delete rows \(individual languages\) from Language Groups as follows.

\[Omitted image "lw-configure-language-groups-delete-rows.png"\] Alt text: In the Language Groups tab, one language group is expanded to show five rows. Check boxes in front of two language rows are selected. The Delete button is highlighted.

1.  In the list of language groups, expand a group to display its rows.
2.  Select the check box of the row you want to delete.
3.  Select the **Delete** button. This button displays the count of rows you have selected.
4.  \(Optional\) You can delete the entire language group by selecting and deleting all of its rows. If you delete only one language, the rest of the group remains.

You can edit a group as follows.

\[Omitted image "lw-configure-language-groups-edit.png"\] Alt text: In the Language Groups tab, one group is expanded to show three rows. The group name in one of the rows is selected, so as to open a modal window.

1.  In the list of language groups, expand a group to display its rows.
2.  Select the name of the group in any one row. The group opens in a modal window.
3.  Select new values from drop-down lists. Use icons to add \(\[Omitted image "plus-outline-24.svg"\]\) or delete \(\[Omitted image "trash-outline-24.svg"\]\) rows.
4.  Select **Edit** to save your updates.

\[Omitted image "lw-configure-language-groups-edit-modal.png"\] Alt text: In the edit modal window of Language Groups, three language rows have add and delete icons along with drop-down lists. The Edit button is highlighted.

**Parent Topic:**[Language setup in Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/lw-language-setup.md)

