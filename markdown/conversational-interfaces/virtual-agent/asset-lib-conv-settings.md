---
title: Conversational settings for Assets in the Asset library
description: Manage asset settings from the Asset library for individual assets.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-11-11"
reading_time_minutes: 1
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Conversational settings for Assets in the Asset library

Manage asset settings from the Asset library for individual assets.

To manage the settings for an asset directly from the Asset library page, select the **Show actions for this row** icon \(![Show actions for this row icon.](../images/icon-show-actions-for-this-row.png)\) and select **Conversational settings**.

![Conversational settings for an asset in the Asset library.](../images/asset-lib-conv-set-01.png)

Use the conversational settings module to edit the settings depending on your asset type. Asset settings vary depending on the asset type. The following table contains the editable settings for each asset type.

|Asset type|Editable settings|
|----------|-----------------|
|Topics|Assistants, Roles, Discoverable \(assistants\), Visible \(assistants\)|
|Subflows|Assistants, Roles|
|Actions|Assistants, Roles|
|Now Assist Custom skills|Assistants, Roles, Discoverable \(assistants\), Visible \(assistants\)|
|AI Agents|Assistants, Roles, Discoverable \(assistants\), Visible \(assistants\)|

![Conversational settings module.](../images/asset-lib-conv-set-02.png)

The following fields are available on the Conversational settings module. Depending on the asset type, you can update the various fields.

<table id="table_jms_fct_ghc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the asset given when creating or editing the asset.

</td></tr><tr><td>

Asset type

</td><td>

Type of the asset.

</td></tr><tr><td>

Link to asset

</td><td>

Select the link to open the asset.

</td></tr><tr><td>

Description

</td><td>

Description of the asset given when creating or editing the asset.

</td></tr><tr><td>

Availability

</td><td>

Availability settings allow you to select the assistants and roles that can access the asset.-   Assistants: Select the assistants that can access the asset. If left empty, the asset can't be used by any assistants.
-   Roles: Select the roles end users must have to access the asset. If left empty, then the asset is available to all roles.

</td></tr><tr><td>

Findability

</td><td>

Findability settings determine whether you can invoke or look for the asset from the chat experience.-   Discoverable: Select the assistants where the asset is discoverable.

If an asset is selected as Discoverable, it’s invoked when matched with the user's utterance.

-   Visible: Select the assistants where the asset is visible.

If an asset is selected as Visible, it appears whenever the **Show me everything** option is selected in the conversation.


</td></tr></tbody>
</table>**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

