---
title: Configure the Localization Framework preferences
description: Configure the preferences to request the translation in the activated languages.
locale: en-US
release: xanadu
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2025-07-28"
reading_time_minutes: 5
breadcrumb: [Localization Framework settings, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the Localization Framework preferences

Configure the preferences to request the translation in the activated languages.

## Before you begin

Role required: localization\_admin or localization\_manager

## Procedure

1.  Navigate to **All** &gt; **Localization Framework** &gt; **Settings**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_hqt_4lv_pnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Identifier of the translation setting.

</td></tr><tr><td>

Artifact

</td><td>

Artifact for the settings being defined.You can select either **All Artifacts** or an artifact of your choice, such as **catalog\_item** or **nlu\_model**.

 **Note:** To select Virtual Agent topics, Document Templates, Document Template Block Content, HTML Document Template, Knowledge Base or Email notification artifacts, you must activate specific plugins. For more information, see [Supported artifacts in Localization Framework](../concept/supported-artifacts-lf.md).

</td></tr><tr><td>

Languages

</td><td>

Target records of the languages available in the instance.All the available languages are populated based on the artifact selected.

</td></tr></tbody>
</table>4.  Select the **Translation Preferences** tab.

5.  On the form, fill in the fields.

<table id="table_nyc_xct_shb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Machine Translation

</td></tr><tr><td>

Enable machine translate

</td><td>

Option to enable the machine translation service for selected languages.**Note:** Dynamic Translation must be installed to use machine translation. For more information, see [Activate Dynamic Translation](../../dynamic-translation/task/activate-dynamic-translation.md).

</td></tr><tr><td>

Translator

</td><td>

List of the available translator services for machine translation. **Note:** Ensure that at least one third-party translator configuration record is integrated and active. For more information, see [Integration with other translation services](../../dynamic-translation/concept/integration-with-other-translation-services.md).

</td></tr><tr><td class="sub-head" colspan="2">

Translation Management System

</td></tr><tr><td>

Enable TMS

</td><td>

Option to enable Translation Management System \(TMS\) for selected languages.

</td></tr><tr><td>

TMS

</td><td>

List of all the TMS services available for machine translation. By default, the **RWS** and the **XTM** TMS are available.

 You can also choose a configured custom TMS. For more information, see [Translation Management System configurations](../concept/tms-configuration.md).

If you are configuring a spoke instance per the Localization Framework Hub and Spoke architecture, select `Localization Framework Hub` in this field. For more information, see [Localization Framework Hub and Spoke architecture](../concept/localization-framework-hub-spoke-architecture.md)

.

</td></tr><tr><td class="sub-head" colspan="2">

Send via Email

</td></tr><tr><td>

Enable send via email

</td><td>

Option to enable email service for content localization for selected languages.

</td></tr><tr><td>

Email subflow

</td><td>

Available subflows for your email. Automatically, a subflow exists. To choose another subflow, create a subflow before setting up the translation preference.

</td></tr><tr><td>

Default file format

</td><td>

Option to select a file format to send and receive the content. By default, XLIFF 1.2 and CSV file formats are supported.

</td></tr><tr><td>

Default recipient\(s\) list

</td><td>

List of recipient email addresses through which the content is sent to the translator for translation.

</td></tr><tr><td class="sub-head" colspan="2">

**Export/Import**

</td></tr><tr><td>

Enable export/import

</td><td>

Option to enable the export and import of content for the translation of selected languages.

</td></tr><tr><td>

Default file format

</td><td>

Available options of file formats to send and receive the content. By default, XLIFF 1.2 and CSV file formats are supported.

</td></tr></tbody>
</table>6.  Select the **Workflow Preferences** tab.

7.  On the form, fill in the fields.

<table id="table_lt1_x3d_qnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workflow

</td><td>

List of all the workflows available for the translation process. For more information on the available workflows, see [Workflows in the Localization Framework](../reference/workflow-localization-framework.md).

</td></tr><tr><td>

Business approver group

</td><td>

List of all the available business approver groups. This field appears only when a workflow that requires business approvals is selected from the **Workflow** field. **Note:** Ensure that the business approver group contains the localization\_fulfiller role.

</td></tr><tr><td>

Localization fulfiller group

</td><td>

List of all the available localization fulfiller groups. **Note:** Ensure that the localization fulfiller group contains the localization\_fulfiller role.

</td></tr><tr><td>

Auto translation mode

</td><td>

Option to select the auto-translation mode. The available options are as follows: -   **Machine Translate**
-   **Send to TMS**. If the instance has been set up as a spoke in the[Localization Framework Hub and Spoke architecture](../concept/localization-framework-hub-spoke-architecture.md), this setting will submit the translation request to the hub.
-   **Send via Email**
For more information, see [Translation Modes](../concept/translation-modes.md) **Note:** Ensure that you have configured the Translation Preferences for the selected auto translation mode.

</td></tr><tr><td>

Translation approver group

</td><td>

List of all the available translation approver groups. This field appears only when a workflow that requires translation approvals is selected from the **Workflow** field. **Note:** Ensure that the translation approver group contains the localization\_fulfiller role.

</td></tr></tbody>
</table>8.  Select the **Project Preferences** tab.

9.  On the form, fill in the fields.

<table id="table_f3x_d5z_ztb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable projects

</td><td>

Option to enable the creation of the localization projects. If this option is enabled if the translation of the artifact is requested, the localization requested items \(LRITMs\) are created. You can then create a project and add the corresponding requested items to start the translation. You must have localization\_manager role to create a project. This option helps in the bulk translation of the artifacts to be done at the same time by adding them to a project. Then, the translation progress of the LRITMs is monitored at the project level.

</td></tr><tr><td>

Enable auto creation

</td><td>

Option to enable the auto creation of the localization projects. If this option is enabled if the translation of the artifact items is requested, then the following occur: -   A localization project is auto created. The corresponding localization requested items \(LRITMs\) are created, bundled, and added to the localization project.
-   The project starts automatically based on the localization framework settings.


</td></tr><tr><td>

Localization manager group

</td><td>

List of all the available user groups. **Note:** Ensure that the localization manager group contains the localization\_manager role.

</td></tr></tbody>
</table>10. Select **Submit**.


**Parent Topic:**[Localization Framework settings](../concept/localization-settings.md)

