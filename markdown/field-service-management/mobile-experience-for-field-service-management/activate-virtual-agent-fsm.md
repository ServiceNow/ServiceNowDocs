---
title: Install Field Service Virtual Agent Conversations
description: You can install the Field Service Virtual Agent Conversations application \(com.sn\_fsm.virtualagent\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence: The application includes conversation topics and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Virtual Agent Conversations, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Install Field Service Virtual Agent Conversations

You can install the Field Service Virtual Agent Conversations application \(com.sn\_fsm.virtualagent\) if you have the admin role. The application includes conversation topics and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Field Service Virtual Agent Conversations requires the following plugins. Ensure that these plugins are activated before you install Field Service Virtual Agent Conversations.
    -   **Required ServiceNow plugins**
        -   **Virtual Agent plugin \(com.glide.cs.chatbot\)**

            Enables the chatbot conversation with virtual agent. For details on activating Virtual Agent, see [Activate Virtual Agent](https://www.servicenow.com/docs/access?context=activate-virtual-agent&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

-   Virtual Agent for Field Service Management requires the following ServiceNow Store applications. Ensure that these applications are installed before you install Field Service Virtual Agent Conversations.
    -   **Required ServiceNow Store applications**
        -   **Field Service NLU Model for Virtual Agent Conversations**

            For more information, see [Enabling NLU](https://www.servicenow.com/docs/access?context=configure-nlu-settings&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).


Role required: admin

## About this task

The Field Service Virtual Agent Conversations provides the following system property.

<table id="table_mdp_cbm_pnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_fsm\_va.days\_in\_past\_to\_debrief\_task

</td><td>

Enable Virtual Agent to debrief the Work in Progress tasks for today and for previous days depending on the selected value. For example, if you select 1 in the **Value** field, the Virtual Agent debriefs the tasks for today and yesterday. If you select 2 in the **Value** field, the Virtual Agent debriefs the task for today, yesterday, and a day before yesterday.

</td></tr></tbody>
</table>The Field Service NLU Model for Virtual Agent Conversation application is installed with Field Service Virtual Agent Conversations:

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Virtual Agent Conversations application \(com.sn\_fsm.virtualagent\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install Field Service Virtual Agent Conversations.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


