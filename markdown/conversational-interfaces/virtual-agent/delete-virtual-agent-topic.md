---
title: Delete a Virtual Agent topic
description: Delete a Virtual Agent topic that is no longer needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/delete-virtual-agent-topic.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Virtual Agent, delete, topic, designer, confirm]
breadcrumb: [Getting started with Assistant Designer Asset library, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Delete a Virtual Agent topic

Delete a Virtual Agent topic that is no longer needed.

## Before you begin

Role required: virtual\_agent\_admin or admin

**Note:** An updated Assistant Designer Asset library user interface is available when you install ServiceNow Otto in Virtual Agent. This content assumes that you can see the list view. If ServiceNow Otto in Virtual Agent is not installed, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/vad-prev-topics-page.md).

## About this task

You can delete a topic using the **Delete** option in the Assistant Designer Asset library or in the topic header bar.

**Note:**

Sometimes, certain categories of topics can’t be deleted, such as the Greeting, Survey, Live Agent, Error, Explore help, and Closing setup topics. Delete option is disabled for subflows, actions, and custom skills.

If you want to remove a topic from your Virtual Agent clients but don't want to delete it, consider making the topic inactive instead.

## Procedure

1.  If you're not working on the topic, navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset Library** tab.

3.  Use one of the following methods based on either a record on the home page or the header inside a topic.

<table id="choicetable_brb_vgj_jcc"><thead><tr><th align="left" id="d138081e160">

Method

</th><th align="left" id="d138081e163">

Description

</th></tr></thead><tbody><tr><td id="d138081e169">

**Asset library - single topic**

</td><td>

Select the show actions for this row icon \[Omitted image "kebab-menu.png"\] Alt text: Show actions for this row icon. on the row for the topic that you want to delete, then select **Delete**.

</td></tr><tr><td id="d138081e189">

**Asset library - multiple topics**

</td><td>

1.  Select the topics that you want to delete.
2.  Select **Delete**.
 **Note:** If one or more of the selected assets are subflows or actions, the delete option is disabled.

</td></tr><tr><td id="d138081e215">

**Topic header bar**

</td><td>

1.  Select a Topic record to open the topic.
2.  Select the topic actions icon \[Omitted image "kebab-menu.png"\] Alt text: Topic actions icon., then select **Delete**.


</td></tr></tbody>
</table>4.  In the Confirm delete dialog box, select **Delete**.

    The tab closes and returns you to the home page.


## Result

A toast message also appears for 4 seconds, confirming the topic has been deleted. You can close the message by selecting the dismiss alert icon \[Omitted image "gray-x-icon.png"\] Alt text:.

If the topic was active and is no longer listed in the home page, the topic is immediately removed from Virtual Agent clients.

**Parent Topic:**[Getting started with Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

