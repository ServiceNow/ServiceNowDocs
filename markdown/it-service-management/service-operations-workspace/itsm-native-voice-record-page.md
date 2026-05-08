---
title: ITSM voice interaction record page
description: The ITSM voice interaction record page provides a component that customers can use for integration with Contact Center as a Service \(CCaaS\) providers and an interface that agents can use to handle customer phone calls.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Configuring Interaction Management in Service Operations Workspace, Configuring Service Operations Workspace for ITSM to improve your experience, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# ITSM voice interaction record page

The ITSM voice interaction record page provides a component that customers can use for integration with Contact Center as a Service \(CCaaS\) providers and an interface that agents can use to handle customer phone calls.

![](../image/chat-hidden-ims.png "ITSM voice interaction record page")

The ITSM voice interaction record page enables CCaaS providers to display native voice integrations in CSM Configurable Workspace. Using CCaaS call controls integrated in the page, agents can do the following:

-   Accept calls directly from the agent inbox.
-   Manage call transfers and conferences.
-   Place calls on hold and on mute.

For more information about the integration with CCaaS providers, see the following topics:

-   
-   [OpenFrame configuration](itsm-native-voice-record-page.md#section_vx4_fzz_kdc)

## Page structure

The ITSM voice interaction record page is made up of two different pages:

-   ITSM voice interaction record page
-   Interaction control page

The pages appear together and are visible to agents for phone interactions when the [OpenFrame configuration](itsm-native-voice-record-page.md#section_vx4_fzz_kdc) is enabled.

The Interaction control page appears in the left panel and includes the following components:

-   [Interaction Controls Component \(ICC\)](itsm-native-voice-record-page.md#section_f2q_wcb_ldc): Enables CCaaS providers to display native voice integrations.
-   [Customer History component](itsm-native-voice-record-page.md#section_imd_r1b_ldc): Displays customer, consumer, or account history information, depending on the customer information provided on the interaction record.
-   [Live call transcript](itsm-native-voice-record-page.md#section_c31_xwz_ydc): Displays the text of the call transcript when a conversation record is present for the interaction.

    **Note:** Live call transcript requires additional configuration.


The CSM voice interaction record page includes the following components:

-   Interaction form
-   [Action bar](itsm-native-voice-record-page.md#section_mjh_fh1_ldc)
-   [contextual side panel component](itsm-native-voice-record-page.md#section_uyq_2l1_ldc)

## Plugin

The CSM voice interaction record page template and page variant are included with the CSM Configurable Workspace application \(com.snc.uib.itsm\_agent\_workspace\).

The CSM voice interaction record page template and page variant are available to users when the Interaction Controls Component plugin \(com.app\_interaction\_control\) is installed.

The Interaction Controls Component plugin has the following dependencies:

-   com.app\_openframe\_store
-   com.sn\_component\_workspace\_openframe

## ITSM voice interaction record template

The ITSM voice interaction record template enables customers to create voice interaction record page variants and customize them as needed. This template includes customizable views for different CCaaS providers as well as real-time updates and notifications.

Record pages and page variants created with this template enable agents to manage phone calls with customers and external users and to display information that helps agents to resolve issues. Use this template to customize and extend ITSM functionality around phone interaction management. Additionally, you can configure a CCaaS provider to integrate features such as call transcript.

## ITSM voice interaction record page variant

The ITSM voice interaction record page variant is included with the ITSM Configurable Workspace plugin and has a dependency on the Interaction Controls Component plugin. This page variant is available for users with the interaction controls enabled. For more information, see [OpenFrame configuration](itsm-native-voice-record-page.md#section_vx4_fzz_kdc).

This page variant includes the following settings.

<table id="table_zqv_lvv_q1c"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Enabling the **Active** check box makes the page variant available to the selected audience. The ITSM voice interaction record page variant is inactive by default.The active setting combined with the page order determines the page that SOW uses to display record information. For more information, see Set record page order.

</td></tr><tr><td>

Order

</td><td>

Each record page has an order which indicates the page priority. The lower the number, the higher the priority.The default order for the ITSM voice interaction record page variant is -2000.

</td></tr><tr><td>

Conditions

</td><td>

Conditions determine when a page variant is displayed. The CSM voice interaction record page variant has the following conditions:-   **table = interaction**: Limits the use of the CSM voice interaction page variant to records from the Interaction \[interaction\] table.
-   **itsm.interactionRecordValid = true**: Checks if the interaction record is available in the database.
-   **itsm.interactionType = phone**: Checks if the **Type** field on the interaction record is set to phone.
-   **itsm.interactiveControlsEnabled = true**: Queries the [OpenFrame configuration](itsm-native-voice-record-page.md#section_vx4_fzz_kdc) record and checks the following:
    -   The **Enable interaction controls** field is enabled.
    -   The user belongs to the group selected in the **User Group** field.

 If all of these conditions are met, the system displays the CSM voice interaction record page variant.

</td></tr><tr><td>

Audience

</td><td>

The audience determines who can see the page variant. The CSM voice interaction record page does not have a defined audience.For more information, see Learn about audiences.

</td></tr></tbody>
</table>To access the settings for this page variant:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  In the Record section of the Pages and variants list, select **ITSM voice interaction record page**.
4.  Select **Settings** at the top of the page.

## ITSM voice interaction record page components

The ITSM voice interaction record page includes the following components.

<table id="table_pk2_g1w_q1c"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Form heading

</td><td>

The form heading displays the interaction short description and also includes the action bar and record tags.

</td></tr><tr><td>

Record tags

</td><td>

Agents can create multiple tags for a record and then use the tags to group and organize records.For more information, see Group and find records using tags in workspace.

</td></tr><tr><td>

[Action bar](itsm-native-voice-record-page.md#section_mjh_fh1_ldc)

</td><td>

The action bar contains the actions available to users while working on phone interaction records.-   **Create**: Create records related to the interaction such as cases, incidents, requests, and consumers.
-   **Save**: Save changes to the interaction record.
-   **More Actions**: Perform additional actions such as starting a discussion and associating a record.

**Note:** The specific actions available are determined by factors such as the user role and other attributes.

</td></tr><tr><td>

[Interaction Controls Component \(ICC\)](itsm-native-voice-record-page.md#section_f2q_wcb_ldc)

</td><td>

The Interaction Controls Component enables CCaaS providers to display native voice integrations. Agents can then use the component to manage customer calls directly from their inbox.For more information, see CSM voice interaction record page.

</td></tr><tr><td>

[Customer History component](itsm-native-voice-record-page.md#section_imd_r1b_ldc)

</td><td>

The Customer History component displays customer, consumer, or account history information, depending on the field selections on the interaction record.This component can also display live call transcript.

**Note:** Live call transcript requires additional configuration.

</td></tr><tr><td>

Interaction details

</td><td>

The interaction details include information about the interaction including the account and contact, short description, and record state.

</td></tr><tr><td>

[Contextual side panel component](itsm-native-voice-record-page.md#section_uyq_2l1_ldc)

</td><td>

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the CSM voice interaction record page includes the following tabs.-   Recommended Actions search
-   Related Lists
-   Attachments
-   Form Templates

</td></tr></tbody>
</table>## Interaction Controls Component \(ICC\)

The Interaction Controls Component appears at the top of the left panel of the CSM voice interaction record page. This component enables CCaaS providers to display native voice integrations. Agents can then use the component to manage customer calls directly from their inbox.

The CSM voice interaction record page with the ICC component is displayed when the following conditions are met:

-   The interaction is of type phone.
-   The **Enable interaction controls** field on the OpenFrame Configuration record is enabled.
-   The agent belongs to the **User Group** selected on the OpenFrame Configuration record.
    -   If a user group is selected on the configuration record, only agents belonging to that group can see the CSM voice interaction record page.
    -   If no group is selected, all agents can see the CSM voice interaction record page.

For more information about the integration with CCaaS providers, see the following topics:

-   
-   [OpenFrame configuration](itsm-native-voice-record-page.md#section_vx4_fzz_kdc)

## Customer History component

The Customer History component appears below the Interaction Controls Component in the left panel. This component is included with the Customer Central plugin, which is activated as part of the SOW application.

The Customer History component includes the **Customer** tab. This tab displays customer, consumer, or account history information, depending on the customer information provided on the interaction record. This tab also includes a search field, filter, and date range selector that agents can use to find specific information in the history.

<table id="table_pyc_pgl_ydc"><thead><tr><th>

Interaction record information

</th><th>

Customer tab information

</th></tr></thead><tbody><tr><td>

Customer information is provided

</td><td>

When a customer is selected on the interaction record and customer history is available, the customer history is displayed in the Customer History tab.If customer history is not available, the Customer History tab displays a message that there is no activity yet.

</td></tr><tr><td>

Customer information is not provided

</td><td>

When a customer is not selected on the interaction record, the Customer History tab displays a message suggesting to link to a customer.

</td></tr><tr><td>

Account information is provided

</td><td>

When an account is selected on the interaction record, the account history is displayed in the Customer History tab.

</td></tr></tbody>
</table>Refreshing the customer history information:

-   When an agent selects a different customer on the interaction record and then saves the record, the agent needs to select **Refresh** on the Customer History component to update the information. The agent can also refresh the record page.
-   If there is new activity while the page is open, the agent needs to refresh the Customer History component or the record page to display the new activity in the Customer HIstory tab. For example, if the agent selects **Create Case** on the interaction record.

## Live call transcript

The Customer History component can be configured to display a **Call Transcript** tab, which shows the live call transcript.

-   This tab displays the text of the call transcript when a conversation record is present for the interaction.
-   This tab displays the following text when a conversation record is not present for the interaction record: Call transcript not available yet.

The Call transcript tab is visible to users if configured in the provider application associated with the interaction.

## Action bar component

The action bar component contains the actions available to users while working on phone interaction records.

**Note:** The specific actions available are determined by factors such as the user role and other attributes.

-   **Create**: Create records related to the interaction.
    -   **Create Case**: Creates a new Case record in a sub tab and adds the record to the Related Tasks and Open Cases related lists.
    -   **Create Incident**: Creates a new Incident record in a sub tab and adds the record to the Related Tasks related list.
    -   **Create Request**: Creates a new Request record in a sub tab and adds the record to the Related Tasks related list.
    -   **Create Problem**: Creates a new Problem record in a sub tab and adds the record to the Related Tasks related list.
    -   **Create Consumer**: Creates a new Consumer record in a sub tab and adds the record to the Consumers list.
-   **Save**: Saves changes to the interaction record.
-   **More Actions**: Perform additional actions such as starting a discussion and associating a record.
    -   **Discuss**: Opens a pop-up window to start a Sidebar discussion.
    -   **Associate Record**: Opens a new record in a sub tab that the agent can use to link a record to the current interaction. This new record is displayed in the Related Tasks related list.

The ITSM voice interaction record page supports actions from the following Customer Service Management and CSM Configurable Workspace plugins:

-   Customer Service \(com.sn\_customerservice\)
-   CSM/FSM Configurable WS Foundation \(com.snc.uib.cwf\_workspace\)
-   CSM Configurable Workspace \(com.snc.uib.csm\_agent\_workspace\)
-   CSM Workspace \(com.snc.agent\_workspace.csm
-   Major Issue Management \(com.sn\_majorissue\_mgt\)
-   Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Customer Service with Request Management \(com.sn\_cs\_sm\_request\)
-   Time Recording for Customer Service \(com.snc.csm\_time\_recording\)
-   Omni-Experience Standard Feature Set

If you are using any additional plugins, you need to add the actions from those plugins to the CSM voice interaction record page action bar. For more information, see the configuration steps in Configure the Front-line case page action bar.

## Contextual side panel component

The ITSM voice interaction record page includes the contextual side panel component, which provides agents with the following functionality.

<table id="table_orh_5rr_m1c"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recommended Actions

</td><td>

The Recommended Actions tab includes AI search in Recommended Actions functionality. Agents can use AI search to find relevant resources or resolutions for customer issues.The search feature displays an initial set of search results based on the text in the interaction short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search.

From the list of search results, agents can select a source to see search results of that type.

Depending on the source type, agents can do the following:

-   Open an article in full view in a sub tab.
-   Flag an article.
-   Mark an article as helpful.
-   Order a catalog item.

For more information, see Use AI search in Recommended Actions to resolve cases.

**Note:** Using Recommended Actions in the contextual side panel requires the Configuring Recommended Actions application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

</td></tr><tr><td>

Related Lists

</td><td>

The Related Lists tab provides access the interaction related lists.The ITSM voice interaction record page incorporates related list functionality into the contextual side panel. These lists appear in an accordion format that agents can expand and collapse as needed.

An indicator displays the number of records available in a related list. When expanded, the records in a related list are displayed in card format.

The ITSM voice interaction record page includes the following related lists:

-   Related Tasks
-   Recent Interactions
-   Open Cases

</td></tr><tr><td>

Attachments

</td><td>

The Attachments tab provides access to case-related attachments. From this tab, agents can view and download attachments.

</td></tr><tr><td>

Templates

</td><td>

The Templates tab provides access to available form templates which enable agents to automatically populate fields on new records. Agents can manually apply a template when creating a new record such as an incident or change.

</td></tr></tbody>
</table>## OpenFrame configuration

The ITSM voice interaction record page variant is included with the SOW application \(com.snc.uib.itsm\_agent\_workspace\). This page variant is available to users when:

-   The Interaction Controls Component plugin \(com.app\_interaction\_control\) is installed.
-   Interaction controls in the OpenFrame configuration are enabled.

Complete the following steps to enable interaction controls:

1.  Navigate to **All** &gt; **OpenFrame** &gt; **Configurations**.
2.  Select a configuration record. For example, select **CTI**.
3.  Select the **Enable interaction controls** check box to enable interaction controls for OpenFrame.
4.  Select a group from the available **User Group** column and move it to the **Selected** column. This is the group of users to whom the OpenFrame configuration applies.
5.  Unlock the URL field, and add a third-party URL.

    You can get this URL from your contact center provider admin.

6.  Select **Update**.

When the following conditions are met, the agent sees the CSM voice interaction record page with the Interaction Controls Component and the Customer History tab component.

-   The interaction is of type phone.
-   The **Enable interaction controls** field on the OpenFrame Configuration record is enabled.
-   The agent belongs to the **User Group** selected on the OpenFrame Configuration record.

The agent can switch between phone interactions and chat interactions. If an interaction is of type chat, the agent sees the CSM default record page.

**Parent Topic:**[Configuring Interaction Management in Service Operations Workspace](configure-interaction-management-sow.md)

