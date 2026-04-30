---
title: Issue Auto Resolution configuration settings
description: Learn about the different configuration settings that you can use for the Issue Auto Resolution \(IAR\) application. For example, you can see the status of your Issue Auto Resolution configurations and decide to turn off or edit each configuration setting to fit your organization's needs.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Using Issue Auto Resolution, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Issue Auto Resolution configuration settings

Learn about the different configuration settings that you can use for the Issue Auto Resolution \(IAR\) application. For example, you can see the status of your Issue Auto Resolution configurations and decide to turn off or edit each configuration setting to fit your organization's needs.

The following tables show the configuration settings that are available for Issue Auto Resolution

**Note:**

To modify your settings, navigate to **All** **&gt; Issue Auto Resolution****&gt; Settings**.

|Setting|Definition|
|-------|----------|
|Table|Name of the table for the Issue Auto Resolution application to process.|
|Invocation type|Trigger for theIssue Auto Resolution application either through a business rule when the case is created or an API on demand.|
|Assign to|Assignee for the case that is being processed by the Issue Auto Resolution application.|
|Requester|User requesting assistance on the issue.|
|Task assignment template|Template that sets the fields and values when it’s being assigned to the user.|
|Task resolution template|Template that sets the fields and values when the user indicates that the issue is resolved.|
|Task completion template|Template that sets the fields and values during the interim state while the matched topic conversation flow runs.|
|Unresolved task template|Template that sets the fields and values when the end user requests agent assistance.|

|Setting|Definition|
|-------|----------|
|Entry conditions|Records that are processed for the Issue Auto Resolution application. Only the issues that match the entry condition are processed by the Issue Auto Resolution application.|
|Exit conditions|Condition where the Issue Auto Resolution application stops processing when the machine learning process is complete.|

|Setting|Definition|
|-------|----------|
|Training language|Language in which the training must be performed for the machine learning model.|
|Configuration languages|Overview of the machine learning models associated with the Issue Auto Resolution configuration.|
|Retrain frequency|Interval in which the machine model must be retrained with the training data.|
|Advanced|Advanced settings that you can enable.|
|Prediction fields|List of fields used as input for processing the issue.|
|Pre-processing extension|Server script to perform data cleanup or manipulation on the issue before it's processed by machine learning APIs. The pre-processing script is available only when your enable the Advanced setting.|
|Post-processing extension|Server script to perform additional actions on the results from machine learning APIs. The post-processing script is available only when you enable the Advanced setting.|

|Setting|Definition|
|-------|----------|
|Apply AI Search|AI search results that are delivered if relevant Virtual Agent topics aren't found.|
|Search application|Detailed AI search settings, including the search source, number of search results to retrieve, and more.|
|Search results portal|Portal to be used in links while delivering recommendations to the users on any response channel.|
|AI Search display topic|Virtual Agent topic that performs AI search and presents the results.|
|EVAM definition|Definition of how search results from different data sources are displayed for the end users in cards and lists.|

|Setting|Definition|
|-------|----------|
|Intent to topic map|List of intents and their associated Virtual Agent topics. When an issue is identified, the corresponding topic is delivered to the user for automatic resolution.|

|Setting|Definition|
|-------|----------|
|Apply AI Search|AI search results that are delivered if relevant Virtual Agent topics aren't found.|
|Search application|Detailed AI search settings, including the search source, number of search results to retrieve, and more.|
|Search results portal|Portal to be used in links when delivering recommendations to the users on any response channel.|
|AI Search display topic|Virtual Agent topic that performs AI search and presents the results.|
|EVAM definition|Definition of how search results from different data sources are displayed for the end users in cards and lists.|

<table id="table_wxn_x2s_dyb"><thead><tr><th>

Setting

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Follow up sequence

</td><td>

Options on how to deliver the deflection content to your users:

 -   **All**: Delivers the deflection content to the user on all available response channels.
-   **First match**: Delivers the deflection content on an active channel where the user is available, in the order defined by the response channels list.

</td></tr><tr><td>

Response channels

</td><td>

List of available response channels to send the user deflection content.

 When you set the **Follow up sequence** to **First match**, the response channel order determines the channel that is used to contact the user. You can adjust the order number to change the priority sequence.

 You must set up the email properties to set **Email** as an active channel.

 The Glide Virtual Agent plugin is required, and Virtual Agent notifications must be enabled to set Chatbot as an active response channel.

 You must configure Twilio Notify to set SMS as an active response channel.

</td></tr><tr><td>

Initial recommendation email

</td><td>

Email template used to deliver the deflection content to users when the AI search recommendations are found.

</td></tr><tr><td>

Catalog submitted email

</td><td>

Email template used to notify users when a catalog item is submitted from recommendations made by the Issue Auto Resolution application.

</td></tr><tr><td>

Notify SMS phone

</td><td>

Twilio Notify phone number to be used to deliver SMS to users.

</td></tr><tr><td>

Initial recommendation SMS

</td><td>

SMS template used to deliver the deflection content to users when AI search recommendations are found.

</td></tr><tr><td>

Catalog submitted SMS

</td><td>

SMS template used to notify users when a catalog item is submitted from recommendations made by the Issue Auto Resolution application.

</td></tr></tbody>
</table><table id="table_ocd_1fs_dyb"><thead><tr><th>

Setting

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Use SLA engine

</td><td>

Task-based SLA engine that provides additional flexibility and functionality.

</td></tr><tr><td>

Auto resolution reminders

</td><td>

List of reminders and the Email and SMS templates used to deliver reminders.

 SLA percentage at which to send the reminder using the Email and SMS templates.

 To send automatic resolution reminders, you must set **Use SLA engine** to **true**.

 **Note:**

The SMS Notification template is only available when the Notify app is installed.

</td></tr><tr><td>

Task SLA

</td><td>

Duration that an issue is assigned to the Issue Auto Resolution application before it’s automatically reassigned to a live agent, if not yet resolved.

</td></tr></tbody>
</table>|Setting|Definition|
|-------|----------|
|Review|Opportunity to review your configuration before you select **Enable IAR**.|

**Parent Topic:**[Using Issue Auto Resolution](auto-resolution-va.md)

