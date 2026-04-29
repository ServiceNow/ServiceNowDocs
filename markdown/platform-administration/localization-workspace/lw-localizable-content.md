---
title: Types of Localizable content in Localization Workspace
description: Localization Workspace collects available translatable content from across your instance when you create a translation request. You can make your content available by configuring permissions and creating an artifact record.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Localization Workspace reference, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Types of Localizable content in Localization Workspace

Localization Workspace collects available translatable content from across your instance when you create a translation request. You can make your content available by configuring permissions and creating an artifact record.

## Prerequisites for availability

The availability of a content type is subject to its table and application scope permissions. Localization Workspace retrieves untranslated or partially translated documents when the following prerequisites are fulfilled.

-   If you have created a custom artifact, set cross-scope privileges to ensure that the corresponding content type can be selected in Localization Workspace. For more information see [Cross-scope privileges for Localization Workspace](../task/lw-cross-scope-privilege.md).
-   If the target tables are restricted, set Restricted Caller Access privileges to ensure that a content type can be selected in Localization Workspace. For more information see [Restricted Caller Access for Localization Workspace](../task/lw-restricted-caller-access.md)
-   For Content Publishing material, add the role sn\_cd.content\_admin to your Localization Workspace group in the sys\_user\_group table. This role is needed to access Content Publishing items from Localization Workspace.

## Translatable content

A document may be considered partially translated when its original is updated after translations were produced. In such cases it may be possible to synchronize the translated versions to the updated original by translating only the new portion of the text.

## Content available by default

The following table lists the content types that are available by default when you install Localization Workspace. These are preconfigured with artifact records and cross-scope permissions.

You can also configure your own custom artifacts. For more information, see [Create and configure a custom artifact](../../localization-framework/task/create-configure-custom-artifact.md).

In this table the **Filter** column shows the query used to retrieve untranslated or partially translated content.

<table id="table_vsv_lp4_52c"><thead><tr><th>

Content type

</th><th>

Table

</th><th>

Filter

</th></tr></thead><tbody><tr><td>

Block Content

</td><td>

sn\_cd\_block

</td><td>

\(No filter. All records.\)

</td></tr><tr><td>

Catalog Item

</td><td>

sc\_cat\_item

</td><td>

active=true^state=published^ORstate=

</td></tr><tr><td>

Document Template Block Content

</td><td>

sn\_doc\_template\_block\_content

</td><td>

active=true

</td></tr><tr><td>

Email Layout Configuration

</td><td>

sys\_email\_layout

</td><td>

\(No filter. All records.\)

</td></tr><tr><td>

Email Notification Configuration

</td><td>

sysevent\_email\_action

</td><td>

active=true

</td></tr><tr><td>

Email Template Configuration

</td><td>

sysevent\_email\_template

</td><td>

\(No filter. All records.\)

</td></tr><tr><td>

HTML Document Template

</td><td>

sn\_doc\_html\_template

</td><td>

active=true

</td></tr><tr><td>

Knowledge

</td><td>

kb\_knowledge

</td><td>

workflow\_state=published^ORworkflow\_state=scheduled\_publish^ORworkflow\_state=pending\_retirement^language=en

</td></tr><tr><td>

News Content

</td><td>

sn\_cd\_content\_news

</td><td>

active=true

</td></tr><tr><td>

Notification Content

</td><td>

sn\_cd\_content\_notification

</td><td>

active=true

</td></tr><tr><td>

Portal Content

</td><td>

sn\_cd\_content\_portal

</td><td>

active=true

</td></tr><tr><td>

To-do Content

</td><td>

sn\_cd\_content\_todo

</td><td>

active=true

</td></tr><tr><td>

NLU Model

</td><td>

sys\_nlu\_model

</td><td>

state=Published^language=en

</td></tr><tr><td>

Survey

</td><td>

asmt\_metric\_type

</td><td>

active=true **Note:** Surveys are an available content type for Localization Workspace from the Yokohama Patch 7 release.

</td></tr><tr><td>

VA Topic

</td><td>

sys\_cs\_topic

</td><td>

active=true

</td></tr></tbody>
</table>**Parent Topic:**[Localization Workspace reference](../concept/localization-workspace-reference.md)

**Related topics**  


[Dynamic artifact detection in Localization Workspace](../concept/lw-dynamic-artifact-detection.md)

[Supported artifacts in Localization Framework](../../localization-framework/concept/supported-artifacts-lf.md)

