---
title: Virtual Agent for HR Service Delivery
description: HR Service Delivery and Virtual Agent provide an automated chat with an employee requesting HR services. You can program Virtual Agent to understand the intent of an employee to handle repeatable requests.Activate Virtual Agent for HR Service Delivery to provide user assistance through a conversational messaging interface. You can also activate Virtual Agent for HR Service Delivery with ServiceNow Natural Language Understanding \(NLU\).Setting up Virtual Agent or Virtual Agent with NLU for HR Service Delivery requires multiple steps.Define a custom HR Service Delivery greeting experience for a specific context in which your users run Virtual Agent. Configure your greeting experience to initiate the virtual agent automatically or immediately transfer to a live agent.HR Service Delivery Virtual Agent provides pre-built patterns that enable you to track whether Virtual Agent conversations helped the end user.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 11
breadcrumb: [Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Virtual Agent for HR Service Delivery

HR Service Delivery and Virtual Agent provide an automated chat with an employee requesting HR services. You can program Virtual Agent to understand the intent of an employee to handle repeatable requests.

Virtual Agent enhances the employee experience by addressing queries immediately.

At any time during a virtual chat, the employee can request to interact with a live HR agent.

For more information, see [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Predefined Virtual Agent topics for HR Service Delivery

The base system provides the predefined Virtual Agent topics \(chatbot conversations\) designed to help your customers complete common self-service HR tasks. These topics are not published and found under the Virtual Agent Designer. For more information, see [Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

For more information on predefined virtual agent topics, see [Prebuilt Virtual Agent topics, topic blocks, and ServiceNow NLU models](https://www.servicenow.com/docs/access?context=prebuilt-topics-ITSM&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

The following predefined, HR Service Delivery Virtual Agent topics are available:

-   Add Emergency Contact \(Template\)
-   Ask a Question \(Template\)
-   Benefits Overview \(Template\)
-   Create HR General Inquiry Case \(Template\)
-   Delete Emergency Contact \(Template\)
-   FAQ Search Fallback Topic \(Template\)
-   General HR Inquiry \(Deprecated\)
-   New Hire Orientation \(Template\)
-   Pay Discrepancy \(Template\)
-   Request for Leave \(Template\)
-   Update Address \(Template\)
-   Update Email \(Template\)
-   Update Emergency Contact \(Template\)
-   Update Phone Number \(Template\)
-   Download Payslip Request \(Template\)
-   Enroll new Beneficiary Request \(Template\)
-   Change in Benefits Inquiry \(Template\)
-   Tuition Reimbursement Request \(Template\)
-   HR Account Access \(Template\)
-   Employment Verification Letter Request \(Template\)
-   401k Benefits inquiry \(Template\)
-   HSA Inquiry \(Template\)
-   Check Case status \(Template\)
-   Employee Info Update \(Template\)

**Note:** Employee info update topic enables you to update information like Email, Address and Phone number, at one place instead of going to the individual topics separately.

**Warning:** General HR Inquiry is no longer available as one of the predefined topics.

A topic defines the dialog between the Virtual Agent \(chat support bot\) and user to accomplish a specific goal. The information exchanged during the conversation flow \(user inputs and bot responses\) enables the chatbot to fulfill a user request or assist a user in completing a task.

For more information, see [Designing a Virtual Agent topic](https://www.servicenow.com/docs/access?context=design-va-topic&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Custom portals and ticket page

If your company has created a custom portal and/or ticket page, and you want the HR case link \(in Virtual Agent\) to redirect to your portal and/or ticket page, then create a system property that links the HR case in Virtual Agent to your portal and/or ticket page. For example:

-   Custom portal name: escServiceNow
-   Custom ticket page name: new\_ticket\_page
-   sys\_property: com.glide.cs.portal\_url\_mapping.escServiceNow.sn\_hr\_core\_case
-   Value: /escServiceNow?id= new\_ticket\_page&amp;sys\_id=\{\{data.sys\_id\}\}
-   Application: Global

**Note:** See [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

## Natural Language Understanding \(NLU\) support

You can set up HR Service Delivery Virtual Agent to use Natural Language Understanding \(NLU\) to understand word meanings and word contexts to infer user or system actions.

For more information about NLU and the NLU Workbench, see [Natural Language Understanding](https://www.servicenow.com/docs/access?context=nlu-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) and [Activate the NLU Workbench](https://www.servicenow.com/docs/access?context=activate-nlu-workbench&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

Also, see [Natural Language Understanding in Virtual Agent](https://www.servicenow.com/docs/access?context=va-NLU&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

**Note:** This feature is only available with the HR Professional and HR Enterprise packages.

## Reusable HR Service Delivery Virtual Agent topic blocks

Create and reuse topic blocks to perform common functions in HR Service Delivery Virtual Agent conversations, like creating an HR case or performing a search.

Topic blocks help you be more productive by minimizing duplicate subflows, are easier to maintain, and ready to use immediately.

The following predefined, reusable topic blocks are:

-   Contextual Search
-   Create HR Case
-   Survey
-   Transfer to Live Agent
-   Update HR Case
-   Employee Authentication
-   Agent Availability
-   FAQ Contextual Search
-   AI Search
-   Request Catalog Item
-   Search Catalog Item
-   Pause

The Topics page in Virtual Agent Designer features a sort tab called **Topic Blocks** for viewing just the reusable topic functions. For detailed information about HR Service Delivery Virtual Agent, refer to [Prebuilt Virtual Agent topics, topic blocks, and ServiceNow NLU models](https://www.servicenow.com/docs/access?context=prebuilt-topics-ITSM&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Integration with messaging applications

Your employees can hold Virtual Agent conversations using Slack, a third-party messaging application.

For more information, see [Virtual Agent integration with messaging apps](https://www.servicenow.com/docs/access?context=va-integration-messaging-apps&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

For information on configuring Virtual Agent notifications for certain channels such as Slack, see [Setting up Virtual Agent notifications](https://www.servicenow.com/docs/access?context=configuring-va-notifications&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Topic Recommendations for HR Service Delivery Virtual Agent

Get pre-built topics or create new topics from the recommended topics for HR Service Delivery Virtual Agent using the default configuration sn\_hr\_core\_case in the Topic Recommendations settings. For more information, see [Topic Recommendations settings](https://www.servicenow.com/docs/access?context=tr-settings-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

![Topic recommendation setting.](../image/topic-recom-setting.png)

For HR Cases, this default setting is shipped with Taxonomy preselected to HRSD and the Filtered by setting set to display the cases created after the last 90 days. For more information on Topic Recommendations, see [Using Virtual Agent Topic Recommendations](https://www.servicenow.com/docs/access?context=va-topic-recommendations&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

In the Topic Recommendations page, under Get new recommendations, select **HR Cases** and click on **Get new recommendations**. Once the new recommendations are available, select your preferred recommendations and add them to the Virtual Agent using the **Add to VA** option. For more information, see [Topic Recommendations page](https://www.servicenow.com/docs/access?context=topic-recommendations-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

**Note:** The system takes around 15 minutes to provide the new topic recommendations.

**Note:**

-   To get the Topic Recommendations, accept the RCAs after installing the HR Service Delivery Virtual Agent plugin.
-   To add a recommended topic to the Virtual Agent, you must be present in the HR Service Delivery Virtual Agent scope.
-   To get Topic Recommendations, make sure there are a minimum of 10,000 records and a maximum of 300,000 records in the HR Cases table.

**Parent Topic:**[Integration of HR Service Delivery with ServiceNow applications](integrate-hr-platform-apps.md)

## Activate Virtual Agent for HR Service Delivery

Activate Virtual Agent for HR Service Delivery to provide user assistance through a conversational messaging interface. You can also activate Virtual Agent for HR Service Delivery with ServiceNow® Natural Language Understanding \(NLU\).

### Before you begin

Role required: admin

### About this task

The HR Service Delivery Virtual Agent Conversations plugin \(sn\_hr\_va\) activates the **sn\_hr\_va.min\_admin\_count** system property in the System Properties \[sys\_properties.list\] table. This property prevents you from deleting your only Virtual Agent admin user by requiring a minimum number of active users with this role. The minimum is two by default.

To activate Virtual Agent, do the following in order:

1.  Activate the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) that provides the Virtual Agent framework.
2.  Activate the Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\) that provides case and knowledge management for HR.
3.  Activate the HR Service Delivery Virtual Agent Conversations plugin \(sn\_hr\_va\) that provides a conversational bot platform for user assistance.

If you want to activate Virtual Agent also with NLU, then activate the following plugins after you have already activated the previous plugins:

1.  Activate the Predictive Intelligence plugin \(com.glide.platform\_ml\) that enables the creation of machine learning solutions.
2.  Activate the NLU Workbench plugin \(com.snc.nlu\_studio\) that enables the creation of NLU models.
3.  Activate the Studio plugin \(com.glide.dev-studio\) that is used for adding and updating application files.
4.  Activate the HR Service Delivery NLU Model for Virtual Agent Conversations plugin \(sn\_hr\_nlu\) that provides the NLU model used by HR Virtual Agent. This plugin is available on the ServiceNow Store, and provides NLU models in the English, German, French, Spanish, Japanese, Dutch, Chinese, and Brazilian Portuguese languages.

**Note:** The HR Service Delivery NLU Models in the Dutch, Chinese and Brazilian Portuguese languages do not support entity extraction \(intent matching and entity recognition\).

When an employee opens an HR case using Virtual Agent for HR Service Delivery, the **Source** field on the HR case is **Virtual Agent**. For more information, see [Work an HR case](../task/t_CreateAnHRCase.md).

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


## Set up Virtual Agent for HR

Setting up Virtual Agent or Virtual Agent with NLU for HR Service Delivery requires multiple steps.

### Before you begin

Role required: admin, virtual\_agent\_admin

The base system provides predefined Virtual Agent and Virtual Agent NLU topics \(chatbot conversations\).

**Note:** You cannot edit the provided topics. You can duplicate a provided topic and then edit it. You can also create additional topics. See [Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

After performing the activation steps, the **Chat** link replaces the **Chat with HR** link on the Employee Center or service portal.

When an employee clicks the **Chat** link, Virtual Agent launches and the employee is chatting with a virtual agent.

Before your employees can use Virtual Agent topics, you must activate and publish them.

Before existing Virtual Agent topics can use NLU, you must republish them.

**Note:** By default, the base system provides topics as inactive and unpublished.

If your company uses a custom service portal and ticket page, see [Virtual Agent for HR Service Delivery](hr-virtual-agent-conversations.md#).

To view, duplicate, preview, or publish HR topics in the Virtual Agent Designer:

### Procedure

1.  Navigate to **All** &gt; **Collaboration** &gt; **Virtual Agent** &gt; **Designer**.

2.  Click **Active** so the button turns green to activate a topic.

3.  Click **Publish**.

4.  Click **Save**.


## Configure a custom HR Service Delivery greeting experience

Define a custom HR Service Delivery greeting experience for a specific context in which your users run Virtual Agent. Configure your greeting experience to initiate the virtual agent automatically or immediately transfer to a live agent.

### Before you begin

Prechat enables you to determine if you want the Virtual Agent topic conversation experience or a live agent experience. The Prechat is independent of the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin activation.

For example, if your instance has both IT Service Management Pro and HR Service Delivery Pro subscriptions, you can implement Virtual Agent topic conversations when a chat starts for ITSM and Live Agent transfer when a chat starts for HR Service Delivery.

You can only customize the greeting experience for Virtual Agent setup topics. Customization of the setup topics is based on the condition that you define. The condition is based on context variables. The customizable setup topics include:

|Setup topic type|Setup topic|
|----------------|-----------|
|Anything else|N/A|
|Live Agent|Live Agent Support|
|Error|Error Handling Topic|
|Greeting|Greetings|
|Closing|Closing Conversation|
|Survey|N/A|
|AI Search fallback|AI Search Fallback|
|Fallback|Fallback Topic|
|Explore Help|Virtual Agent Capabilities|

Role required: virtual\_agent\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Select Virtual Agent.

3.  In Custom Greetings and Setup, select **View all**.

4.  Select **New**.

5.  On the Custom Greetings and Setup form, fill in the fields.

    For field descriptions and more details, see [Configure a Virtual Agent chat experience](https://www.servicenow.com/docs/access?context=configure-default-chat-experience&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

    **Note:** Define the custom experience in the **Provide the context** section of the Custom Greetings and Setup record. Configure the **Condition Mode** field to **Advanced** and customize the condition logic in the **Script** field with JavaScript that specifies the context.

6.  Select **Create custom experience**.


### Result

You have created a custom greeting experience for HR Service Delivery users.

**Note:** A custom greeting and chat experience HR ESC Experience is available to the HR Service Delivery Virtual Agent users to cater to HR Service Delivery specific search experience. This experience is inactive by default, you have to activate it for your users.

## Capturing solution delivery in HR Service Delivery Virtual Agent chats

HR Service Delivery Virtual Agent provides pre-built patterns that enable you to track whether Virtual Agent conversations helped the end user.

Deflection outcomes indicate whether Virtual Agent chats provided a solution to the user. You can define deflection points in a Virtual Agent topic that can be mapped to a deflection pattern to capture the right deflection.

For HR Service Delivery Virtual Agent users, six deflection patterns are available by default. They are divided into three deflection outcomes:

-   Confirmed deflection - Provides a resolution to the user that prevents the user from creating an HR case or transferring to a live agent. For example, Virtual Agent might add a user to the distribution list.
-   Potential deflection - Provides a partial resolution to the user. For example, information the user is looking for is provided or search results are returned.
-   No deflection - Did not provide a solution or the user created a general inquiry case.

|Deflection patterns|Activity|Deflection outcomes|
|-------------------|--------|-------------------|
|HR VA Search-Served|Knowledge base article served and helped|Confirmed deflection|
|HR VA Self-Resolving|Information updated|Confirmed deflection|
|HR VA Triage&amp;Created|HR service case created|Potential deflection|
|HR VA Info-Found|Information found|Potential deflection|
|HR VA Service Case Not Created|HR general inquiry case created|No deflection|
|HR VA Info-Not-Found|Information not found|No deflection|

If the user interacts with a Virtual Agent topic that has deflection defined, the deflection data is captured automatically in the background without changing the user experience. This deflection outcome of matched patterns is then recorded for analysis. You can access this information by navigating to **All** &gt;**Self-Service Analytics** &gt; **Deflection Metric**.

**Note:** The default deflection patterns in the HR Service Delivery Virtual Agent are not customizable. To modify a deflection pattern, you have to clone it, make the necessary changes, activate it and then publish the pattern.

