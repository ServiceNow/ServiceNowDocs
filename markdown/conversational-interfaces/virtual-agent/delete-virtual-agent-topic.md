---
title: Delete a Virtual Agent topic
description: Delete a Virtual Agent topic that is no longer needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/conversational-interfaces/virtual-agent/delete-virtual-agent-topic.html
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-15"
reading_time_minutes: 2
keywords: [Virtual Agent, delete, topic, designer, confirm]
breadcrumb: [Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Delete a Virtual Agent topic

Delete a Virtual Agent topic that is no longer needed.

## Before you begin

Role required: virtual\_agent\_admin or admin

**Note:** An updated Virtual Agent Designer user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not enabled, you will see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/conversational-interfaces/virtual-agent/vad-prev-topics-page.md).

## About this task

You can delete a topic using the **Delete** option on the Virtual Agent Designer home page or in the header bar for the topic.

**Note:**

Sometimes, certain categories of topics can’t be deleted, such as the Greeting, Survey, Live Agent, Error, Explore help, and Closing setup topics. Delete option is disabled for subflows, actions, and custom skills.

If you want to remove a topic from your Virtual Agent clients but don't want to delete it, consider making the topic inactive instead.

## Procedure

1.  If you're not working on the topic, navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer** to display the home page.

2.  Use one of the following methods based on either a record on the home page or the header inside a topic.

<table id="choicetable_brb_vgj_jcc"><thead><tr><th align="left" id="d110981e147">

Method

</th><th align="left" id="d110981e150">

Description

</th></tr></thead><tbody><tr><td id="d110981e156">

**Home page - single topic**

</td><td>

Select the show actions for this row icon \[Omitted image "kebab-menu.png"\] Alt text: KB link on the row for the topic that you want to delete, then select **Delete**.

</td></tr><tr><td id="d110981e172">

**Home page - multiple topics**

</td><td>

1.  Select the topics that you want to delete.
2.  Select **Delete**.
 **Note:** If one or more of the selected assets are subflows or actions, the delete option is disabled.

</td></tr><tr><td id="d110981e196">

**Topic header bar**

</td><td>

1.  Select a Topic record to open the topic.
2.  Select the topic actions icon \[Omitted image "kebab-menu.png"\] Alt text: KB link, then select **Delete**.


</td></tr></tbody>
</table>3.  In the Confirm delete dialog box, select **Delete**.

    The tab closes and returns you to the home page.


## Result

A toast message also appears for 4 seconds, confirming the topic has been deleted. You can close the message by selecting the dismiss alert icon \[Omitted image "gray-x-icon.png"\] Alt text: Dismiss alert icon..

If the topic was active and is no longer listed in the home page, the topic is immediately removed from Virtual Agent clients.

**Parent Topic:**[Getting started with Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

