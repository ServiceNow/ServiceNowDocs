---
title: Filter content by label for a Google Drive external content connector
description: Configure a label filter for your Google Drive external content connector. The connector only retrieves content that has one or more of your specified label values applied.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/filter-content-label-google-drive-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-06-26"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Google Drive external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Filter content by label for a Google Drive external content connector

Configure a label filter for your Google Drive external content connector. The connector only retrieves content that has one or more of your specified label values applied.

## Before you begin

Role required: admin

## About this task

The Google Drive external content connector supports the use of labels to filter retrieved content. You can specify a list of label value IDs for your Google Drive connectors to check for during content crawls. The connectors only retrieve content items that have one or more of your specified label values applied.

**Note:** This task is optional. If you don't specify a list of label value IDs, your Google Drive connectors ignore labels when retrieving content items.

To learn more about labels and their IDs and values in Google Drive, see the [Labels overview](https://developers.google.com/workspace/drive/api/guides/about-labels) Google developer guide.

## Procedure

1.  Navigate to the External Content Connector Configuration Tables \[sn\_ext\_conn\_base\_connector\_configuration\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sn_ext_conn_base_connector_configuration.list`.

    3.  Press Enter.

2.  If the Advanced Configuration field doesn't appear in the list view, add it to the list view.

    1.  Select the Personalize List icon \[Omitted image "gear.png"\] Alt text:.

    2.  In the Personalize List Columns dialog box, find the Advanced Configuration field in the Available list and use the Add icon \[Omitted image "icon-slushbucket-add.png"\] Alt text: to move it to the Selected list.

    3.  Select **OK**.

3.  Use the list editor to add the **google\_drive\_label\_include\_filter** property to the Advanced Configuration field value.

    To learn more about the list editor, see [Use the list editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_UseTheListEditor.md).

    1.  Double-click or long-press \(or use the keyboard shortcut\) to open the Advanced Configuration field value.

        The list editor pane opens and displays the current field value.

    2.  In the Advanced Configuration JSON object literal, add this new JSON property.

        ```json
        "google_drive_label_include_filter": [ "label_id_1" ]
        ```

    3.  Inside the brackets for the new JSON property's array value, replace the placeholder `"label_id_1"` string with a comma-separated list of label value IDs that you want Google Drive external connectors to use as filters when retrieving content.

        As an example, you might replace `"label_id_1"` as follows to filter on three label values with the specified IDs:

        ```json
        "google_drive_label_include_filter": [ 
           "0Nlvb5ey59iFqWKEF8r8JjE2TykSaYY87y8RNNEbbFcb",
           "EmOlI66ZEgwIbZH2iDvPTbAQ4lGEETKf363RNNEbbFcb",
           "LXpSpR3Tedghc59mo8hE3MiWsG4Xxqi2bzeSNNEbbFcb"
        ]
        ```

        With this JSON property specified, your Google Drive connectors only retrieve content items that have at least one of the three specified label values applied.

        **Note:** To find the ID for a Google Drive label value, edit the label value in Google Drive. The label value's ID appears in the **Label details** section of the **Preview** pane on the editor page. For details on editing labels in Google Drive, see the [Edit and monitor classification labels for your organization](https://knowledge.workspace.google.com/admin/security/edit-and-monitor-classification-labels-for-your-organization) Google Workspace Help resource.

    4.  Select the Save icon \[Omitted image "IconSave.png"\] Alt text: or press Enter.

        The list editor pane closes and the field value is updated with your changes.


## Result

When you run content crawls for your Google Drive external content connectors, the connectors only retrieve content items that have one or more of your specified label values applied.

**Parent Topic:**[Google Drive external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/google-drive-external-content-connector.md)

