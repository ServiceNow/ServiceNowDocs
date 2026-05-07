---
title: Configure Now Assist in Conversational Catalog Request
description: Speed up and provide a conversational and streamlined experience based on generative AI while submitting a catalog item request in Virtual Agent. Your organization can increase self-service and reduce operating costs.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Now Assist in Conversational Catalog Request, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Now Assist in Conversational Catalog Request

Speed up and provide a conversational and streamlined experience based on generative AI while submitting a catalog item request in Virtual Agent. Your organization can increase self-service and reduce operating costs.

## Before you begin

Role required: admin or catalog\_admin, and flow\_designer \(to edit the subflow\)

## About this task

Generative AI capabilities are leveraged to provide a human-like and efficient catalog request experience over the Virtual Agent conversational interface. It reduces the turnaround time for the request submission.

When the generative AI experience is configured for catalog item request submission, the following experience is available for a requester:

-   Contextual question prompts that enable a more human-like conversation based on answers to previous questions.
-   Slot filling that recognizes answers to 1 or more questions on the requester's input. For example, if the search keyword is `I’d like to request for a Windows Virtual Machine with 1TB disk space` and if the catalog item has questions about operating system and hard disk space, then the requester doesn't have to answer these questions again.
-   Ability to answer multiple catalog item questions at the same time.
-   Multi-turn catalog ordering where requesters can change answers at any point. For example, while answering a question about a phone's memory size, the requester can mention about changing the phone model selected in the previous question.
-   Validation of questions' answers.
-   Ability to exit the request submission process at any point.

**Note:**

-   Read-only questions, questions with pre-filled answers, and questions that are already answered in the requester’s search keyword are skipped.
-   Though the following catalog item question types are supported in the conversation mode, natural language responses aren't supported for them:
    -   Attachment
    -   Masked

## Procedure

1.  To configure the Now Assist for Virtual Agent application that installs the Now Assist in Conversational Catalog Request application, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

    With this configuration, the **sn\_now\_assist\_cr.llm.conversational.request.question.limit** system property value is set to 500 by default if that property wasn't edited earlier.

2.  Enable the generative AI experience for a catalog item request submission in Virtual Agent.

    1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Maintain Items**.

    2.  Select a catalog item that must be requested in the conversation mode.

        For information about catalog items that are supported in the conversation mode, see [Topic blocks to request catalog items through conversational experience](../concept/request-topic-blocks-va-llm.md).

    3.  On the catalog item form, confirm that the **Make the item non-conversational in VA** check box isn’t selected.

    4.  On the catalog item form, confirm that the **Turn off Now Assist \(LLM\)** check box isn't selected.

        If you select this check box, LLM isn’t used and the data isn't sent to LLM. The item might become non-conversational.

        **Note:**

        -   If you want the catalog item non-conversational, then select the **Make the item non-conversational in VA** check box. But if the catalog item contains some sensitive information that you don’t want to send to LLM, then select the **Turn off Now Assist \(LLM\)** check box.
        -   If you clear the **Make the item non-conversational in VA** check box, the item will become conversational only if all the conditions are met for making an item conversational. For more information about such conditions, see [Topic blocks to request catalog items through conversational experience](../concept/request-topic-blocks-va-llm.md).
    5.  Select **Update**.

3.  Confirm that the fallback record producer is configured in the **Fetch generic ticket producer for conversational catalog request** subflow.

    In a few cases, when a requester is searching for a catalog item, AI Search might not be able to return any results. For example, when the catalog item isn't available or when the requester has no access to view the catalog item. In such cases, the fallback mechanism is activated for the Virtual Agent conversation. Virtual Agent tries to connect the requester to a live agent. If a live agent isn't available, then the **Create a generic ticket** record producer, which creates an incident to resolve the issue, is triggered.

    -   The **Now Assist Fallback** topic controls the fallback mechanism. This topic triggers the record producer returned by the **Fetch generic ticket producer for conversational catalog request** subflow.
    -   This subflow returns the value of the **sn\_nowassist\_va.now.assist.generic.ticket.fallback.record.producer** property. By default, this property's value is the sys\_id of the **Create a generic ticket** record producer.
    **Note:** Both the **sn\_nowassist\_va.now.assist.generic.ticket.fallback.record.producer** property and the **Create a generic ticket** record producer are available in an instance when the Now Assist for Virtual Agent application is installed.

    Additionally, you can customize the fallback process by configuring your own record producer or by building additional logic in a new subflow.

<table id="choicetable_omj_3fl_lzb"><thead><tr><th align="left" id="d547437e322">

Option

</th><th align="left" id="d547437e325">

Description

</th></tr></thead><tbody><tr><td id="d547437e331">

**Configure your own record producer. For example, to change the inputs in a Virtual Agent conversation.**

</td><td>

1.  Navigate to **sys\_properties.list**.
2.  Select the **sn\_nowassist\_va.now.assist.generic.ticket.fallback.record.producer** property.
3.  In the **Value** field, enter the sys\_id of the record producer that you want to refer to.
4.  Select **Update**.


</td></tr><tr><td id="d547437e370">

**Build additional logic in a new subflow. For example, to refer to a new record producer for each business.**

</td><td>

1.  Create a subflow to return the sys\_id of a record producer. For information about Flow Designer subflows, see [Building subflows](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).
2.  Navigate to **sys\_properties.list**.
3.  Select the **sn\_nowassist\_va.now.assist.generic.ticket.fallback.subflow** property.
4.  In the **Value** field, enter the scope and internal name of the subflow. For example, **global.subflow\_name**. Locate the **Internal name** field in the list of Flow Designer subflows.

**Note:** By default, the value of this property is **sn\_nowassist\_va.fetch\_generic\_ticket\_producer\_for\_conversational\_catalog\_request**.

.

5.  Select **Update**.


</td></tr></tbody>
</table>4.  Configure URL navigation settings to specify where the generated ticket link in the Virtual Agent chat opens, see [Configure URL navigation for chat links](https://www.servicenow.com/docs/access?context=ac-configure-url-navigation&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

    For information about URL navigation in Virtual Agent, see [URL navigation in Conversational Interfaces](https://www.servicenow.com/docs/access?context=url-navigation-ci&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US). For information about Virtual Agent scripts, see [Virtual Agent scripts](https://www.servicenow.com/docs/access?context=virtual-agent-scripts&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

    ![Generated ticket link in the Virtual Agent chat](../../../administer/now-assist-in-va/image/va-link-cat-item.png "Generated ticket link in the Virtual Agent chat")


**Parent Topic:**[Now Assist in Conversational Catalog Request](../concept/now-assist-in-conversational-catalog-request.md)

