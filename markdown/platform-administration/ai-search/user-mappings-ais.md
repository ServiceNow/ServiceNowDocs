---
title: Mapping external users and groups to ServiceNow AI Platform users
description: AI Search external user mappings enable you to configure externally defined user and group aliases for ServiceNow AI Platform users. AI Search uses these aliased security principals to apply content security filters that control user access to search results indexed from external documents.AI Search user mapping aliases can include externally defined group and user security principals.Define a table to store externally defined user and group aliases for ServiceNow AI Platform users.Specify the user mapping table you want AI Search to use for external documents ingested through an indexed source.You can use the AI Search External User Mapping API to import mappings between ServiceNow AI Platform users and externally defined users and groups.Review the results for your user mapping import operations, including data, log messages, and any errors. Use this procedure to verify that your user mappings are imported correctly.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-05-14"
reading_time_minutes: 7
breadcrumb: [External content security, Indexing and searching external content, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Mapping external users and groups to ServiceNow AI Platform users

AI Search external user mappings enable you to configure externally defined user and group aliases for ServiceNow AI Platform users. AI Search uses these aliased security principals to apply content security filters that control user access to search results indexed from external documents.

You can use mapped external user and group names when defining access permissions for external documents that you ingest for indexing via the [External Content Ingestion API](https://www.servicenow.com/docs/access?context=external-content-ingestion-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

## External content security user mapping overview

To configure user mappings for external content security, you must perform the following steps:

1.  Create one or more user mapping tables. For instructions on this procedure, see [Create a user mapping table](user-mappings-ais.md#).
2.  Link a user mapping table to each of your external content indexed sources. For details on this task, see [Link a user mapping table to an external content indexed source](user-mappings-ais.md#).

    **Note:** If no mapping is found for the current ServiceNow AI Platform user, AI Search only allows the user to view search results for external documents that have the **everyone** permission set to true. This can occur if no user mapping table is linked to a search result's indexed source, or if no mapping for the current ServiceNow AI Platform user exists in the indexed source's linked user mapping table.

3.  Import user mappings into your user mapping tables with the [AI Search External User Mapping API](https://www.servicenow.com/docs/access?context=ext-user-mapping-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

Users with the ais\_high\_security\_admin role can review history records for import operations to verify that user mappings imported correctly. For instructions on this procedure, see [View history records for user mapping import operations](user-mappings-ais.md#).

**Parent Topic:**[External content security for AI Search](external-content-security-ais.md)

## External user mapping security principal types

AI Search user mapping aliases can include externally defined group and user security principals.

<table id="table_wqh_q5p_5pb"><thead><tr><th>

Mapped security principal type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Externally defined group

</td><td>

The ServiceNow AI Platform® user specified in the user mapping inherits group-level access permissions for all aliased external groups. For example, if you define external group **report-users** as an alias for ServiceNow AI Platform user **beth.anglin@example.com**, AI Search allows **beth.anglin@example.com** to view indexed search results for external documents that include read access permission for **report-users**.

</td></tr><tr><td>

Externally defined user

</td><td>

The ServiceNow AI Platform user specified in the user mapping inherits user-level access permissions for all aliased external users. For example, if you define external user **ad\\abel-tuter** as an alias for ServiceNow AI Platform user **abel.tuter@example.com**, AI Search allows **abel.tuter@example.com** to view indexed search results for external documents that include read access permission for **ad\\abel-tuter**.

</td></tr></tbody>
</table>## Create a user mapping table

Define a table to store externally defined user and group aliases for ServiceNow AI Platform® users.

### Before you begin

The External Content for AI Search plugin \(com.glide.ais.external\_content\) must be activated in your instance.

Role required: ais\_admin

### About this task

User mapping tables store user mappings for use with external documents that have access permissions. Each mapping specifies externally defined user and group aliases for an individual ServiceNow AI Platform user. AI Search uses the mappings linked to an external document's indexed source to determine whether a ServiceNow AI Platform user can view the indexed record for the document.

All user mapping tables extend the AI Search External Search User Mapping Base \[ais\_external\_search\_user\_mapping\] table.

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **External Content** &gt; **Create User Mapping**.

2.  Enter a name for your user mapping table.

3.  Select **Submit**.

    The dictionary form for your new user mapping table appears.


### What to do next

Import user mappings into your new user mapping table. For an overview of this process, see [Importing user mappings](user-mappings-ais.md#). For details on the relevant API endpoint, see [AI Search External User Mapping API](https://www.servicenow.com/docs/access?context=ext-user-mapping-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

## Link a user mapping table to an external content indexed source

Specify the user mapping table you want AI Search to use for external documents ingested through an indexed source.

### Before you begin

The External Content for AI Search plugin \(com.glide.ais.external\_content\) must be activated in your instance.

The source table for the indexed source must be an external content schema table.

Role required: ais\_admin

### About this task

A user mapping table linked to an indexed source defines external user and group aliases for ServiceNow AI Platform® users. AI Search uses these aliases to determine a user's effective access permissions when their search matches a record from the indexed source.

A user mapping table can be linked to any number of indexed sources.

**Note:** If no mapping is found for the current ServiceNow AI Platform user, AI Search only allows the user to view search results for external documents that have the **everyone** permission set to true. This can occur if no user mapping table is linked to a search result's indexed source, or if no mapping for the current ServiceNow AI Platform user exists in the indexed source's linked user mapping table.

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the indexed source record that you want to link a user mapping to.

3.  In the AI Search External Search User Mapping Table Data Source Relationships related list, create a new relationship record for the user mapping table that you want to link to the indexed source:

    1.  Select **New**.

    2.  On the AI Search External Search User Mapping Table Data Source Relationship form, fill in the fields.

    3.  Select **Submit**.

        The user mapping table's name appears in the related list.


## Importing user mappings

You can use the AI Search External User Mapping API to import mappings between ServiceNow AI Platform® users and externally defined users and groups.

To define a user mapping for import, you need the following information:

-   The email address that uniquely identifies a ServiceNow AI Platform user in the User \[sys\_user\] table.
-   The list of externally defined groups that you want to alias to the ServiceNow AI Platform user. This list can be empty.
-   The list of externally defined users that you want to alias to the ServiceNow AI Platform user. This list can be empty.

For more information on importing user mappings, see [AI Search External User Mapping API](https://www.servicenow.com/docs/access?context=ext-user-mapping-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

## View history records for user mapping import operations

Review the results for your user mapping import operations, including data, log messages, and any errors. Use this procedure to verify that your user mappings are imported correctly.

### Before you begin

Role required: ais\_admin, ais\_high\_security\_admin, and import\_transformer.

### About this task

AI Search creates an import set for each batch of user mappings that you import via the [AI Search External User Mapping API](https://www.servicenow.com/docs/access?context=ext-user-mapping-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US). The transform histories for these import sets provide insight into the results of your user mapping import operations.

### Procedure

1.  Elevate to the ais\_high\_security\_admin role:

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

2.  Navigate to **All** &gt; **AI Search** &gt; **External Content** &gt; **User mapping import history**.

3.  Review each user mapping import history record that you're interested in.

    1.  Open the user mapping import history record.

    2.  On the AI Search External Content User Mapping History Record form, select the **Show Transform History** related link.

        The Transform History \[sys\_import\_set\_run\] table opens, with a filter applied for the import set from the selected user mapping import history record.

    3.  Open the transform history record.

    4.  Review import set results on the form, errors in the Import Set Row Errors related list, and log messages in the Import Log related list.


