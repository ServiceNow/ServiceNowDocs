---
title: Get help using virtual agent conversations from Business Portal
description: Predefined Customer Service Virtual Agent chatbot conversations help your customers complete common self-service tasks, such as getting help with a product or checking the status of a case. Use predefined NLU with your virtual agent chatbot topics to assess the intent of the user input and provide the best response based on the context of the conversation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Business Portal, Customer communication, Use, Customer Service Management]
---

# Get help using virtual agent conversations from Business Portal

Predefined Customer Service Virtual Agent chatbot conversations help your customers complete common self-service tasks, such as getting help with a product or checking the status of a case. Use predefined NLU with your virtual agent chatbot topics to assess the intent of the user input and provide the best response based on the context of the conversation.

## Before you begin

Role required: sn\_customerservice.customer, sn\_customerservice.consumer

If you’re anonymous \(not logged in to the application\), get help by entering keywords for an issue and choose to get transferred to a live agent.

Install the plugin Customer Service Virtual Agent Conversations \(ID: com.sn\_csm.virtualagent\) to view the chatbot topics.

A user with a proxy\_contact role can also check the case status for a customer.

## About this task

The information exchanged during the conversation flow \(user inputs and bot responses\) enables the chatbot to fulfill a user request or assist a user in completing a task. If the user has a question or an issue with an existing product or order, the virtual agent searches the keyword and displays relevant knowledge articles that can help resolve the issue. If there are no relevant articles, it creates a case.

ServiceNow NLU enables discovery of the chatbot topics based on either the keywords entered in the chat or the user-intent and matches an entity with the user input. It also makes the entity available to the topic if there’s a match.

## Procedure

1.  Navigate to the business portal.

2.  Select **Chat**.

    You can select **Show Me Everything** to display all available topics or enter keywords to narrow down the results to relevant topics.

3.  If you’re a logged-in user, enter keywords to get help on a case, an issue, or an order.

    -   If NLU is enabled, it guides you through the right topic based on the utterance.
    -   If NLU isn’t enabled, it displays topics based on the match for the entered keywords. You can make a selection from all available topics displayed.
    **Note:** Contact your administrator to determine whether the topics are NLU-enabled.

4.  Use

<table id="choicetable_cfq_4xm_rgb"><thead><tr><th align="left" id="d313443e133">

To

</th><th align="left" id="d313443e136">

Follow these steps

</th></tr></thead><tbody><tr><td id="d313443e142">

**Check the status of a case**

</td><td>

1.  Initiate checking the case status.
    -   If you’re using the virtual agent conversation without enabling NLU, select **Check Case Status**.
    -   If you’re using NLU in your virtual agent conversation, enter an utterance to check the status of a case.

**Note:** If you provide a case number, you’ll be presented with the details of the case.

2.  Select a case from the case list that you would like to get help for.
3.  When the case information displays, you can do one of the following:
    -   Add a comment
    -   Attach a picture
    -   Check another case
    -   Contact an agent.


</td></tr><tr><td id="d313443e190">

**Get help with a product**

</td><td>

Enter a keyword for your issue. The chatbot returns a list of related knowledge articles to help resolve your issue. If there are no matching articles associated with the description, a case is automatically created with the following information:

-   Case identification number
-   Short description
-   State
-   Priority
 Take any of the following additional actions:

-   Update the product and asset
-   Add a comment
-   Attach a picture
-   Contact an agent


</td></tr><tr><td id="d313443e233">

**Get help**

</td><td>

If you’re an anonymous user not logged in to the application, enter keywords for your issue. The chatbot returns a list of related knowledge articles that have been made public. If there are no matching articles that would help resolve the issue, you can choose to be transferred to a live agent.

</td></tr><tr><td id="d313443e245">

**Submit Request**

</td><td>

1.  Initiate submitting your request for one of the catalog items.
    -   If you’re using the virtual agent conversation without enabling NLU, select **Show Me Everything** and then select **Submit a request**.
    -   If you’re using NLU in your virtual agent conversation, enter an utterance for example open a request, that will identify that there is a NLU and intent associated.
2.  Select the catalog item. The Search Catalog Item topic block searches for the catalog item and displays a link based on your search. For more information about search catalog item, see ITSM Virtual Agent

**Note:** Wherever the topic is opened, the records will display on the same portal.

3.  Click on the link displayed and exit the virtual agent if you do not have any further request.


</td></tr><tr><td id="d313443e287">

**Create Case**

</td><td>

Creates a case from Virtual Agent. You need the following fields to create a case:

-   short\_description \(mandatory\)
-   description
-   account\_sys\_id
-   contact\_sys\_id
-   consumer\_sys\_id
The values of these can be empty. If the account, contact, and consumer fields are empty, the logged in user details are populated. The topic block returns the variable case\_sys\_id from the toic block.

</td></tr><tr><td id="d313443e317">

**Update Case**

</td><td>

Updates a case from Virtual agent. You need the following 2 fields to update a case:

 -   case\_sys\_id \(mandatory\) - must be a valid case ID. If the ID is valid the following 4 options are displayed:
    -   Add product information is displayed only if enable\_product\_update is set to true.
    -   Add a comment
    -   Attach an image
    -   Cancel
-   enable\_product\_update - If set to true, the Add product information option is displayed. It updates the asset and model information.
The topic block returns the variable case\_sys\_id

</td></tr></tbody>
</table>5.  To exit a chat conversation, select **I'm done**.


**Related topics**  


[Customer Service Virtual Agent conversations](../concept/csm-virtual-agent-chatbot.md)

[bundle-convint.topic-blocks-overview]

