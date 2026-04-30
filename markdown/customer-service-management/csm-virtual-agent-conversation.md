---
title: Get help using virtual agent conversations
description: Predefined Customer Service Virtual Agent chatbot conversations help your customers complete common self-service tasks, such as getting help with a product or checking the status of a case. Use predefined NLU with your virtual agent chatbot topics to enable the chatbot to assess the intent of the user input and provide the best response based on the context of the conversation.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Using the Customer Service Portal, Customer communication, Using Customer Service Management, Customer Service Management]
---

# Get help using virtual agent conversations

Predefined Customer Service Virtual Agent chatbot conversations help your customers complete common self-service tasks, such as getting help with a product or checking the status of a case. Use predefined NLU with your virtual agent chatbot topics to enable the chatbot to assess the intent of the user input and provide the best response based on the context of the conversation.

## Before you begin

Role required: sn\_customerservice.customer, sn\_customerservice.consumer

If you are an anonymous user not logged into the application, you can get help by entering keywords for an issue and choose to get transferred to a live agent.

A user with a proxy\_contact role can also check the case status for a customer.

## About this task

The information exchanged during the conversation flow \(user inputs and bot responses\) enables the chatbot to fulfill a user request or assist a user in completing a task. If the user has a question or an issue with an existing product or order, the virtual agent searches the keyword and displays relevant knowledge articles that can help resolve the issue. If there are no relevant articles, it creates a case.

ServiceNow NLU enables discovery of the chatbot topics based on either the keywords entered in the chat or the user-intent and matches an entity with the user input. It also makes the entity available to the topic if there is a match.

## Procedure

1.  Navigate to the Customer Service Management portal.

2.  Click **Chat**.

    You can click **Show Me Everything** to display all available topics or enter keywords to narrow down the results to relevant topics.

3.  If you are a logged-in user, enter keywords to get help on a case, an issue, or an order.

    -   If NLU is enabled, it will guide you through the right topic based on the utterance.
    -   If NLU is not enabled, it will display topics based on the match for the entered keywords. You can make a selection from all available topics displayed.
    **Note:** Contact your system administrator to determine whether the topics are NLU-enabled.

4.  Use

<table id="choicetable_cfq_4xm_rgb"><thead><tr><th align="left" id="d242658e143">

To

</th><th align="left" id="d242658e146">

Follow these steps

</th></tr></thead><tbody><tr><td id="d242658e152">

**Check the status of a case**

</td><td>

1.  Initiate checking the case status.
    -   If you are using the virtual agent conversation without enabling NLU, click **Check Case Status**.
    -   If you are using NLU in your virtual agent conversation, enter an utterance to check the status of a case.

**Note:** If you provide a case number, you will be presented with the details of the case.

2.  Select a case from the case list that you would like to get help for.
3.  When the case information displays, you can do one of the following:
    -   Add a comment
    -   Attach a picture
    -   Check another case
    -   Contact an agent.


</td></tr><tr><td id="d242658e212">

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


</td></tr><tr><td id="d242658e261">

**Get help with an order**

</td><td>

1.  Initiate checking the status of your order.
    -   If you are using the virtual agent conversation without enabling NLU, click **Get Help with Order**.
    -   If you are using NLU in your virtual agent conversation, enter an utterance to get help on an order.

**Note:** If you provide an order number, you will be presented with the details of the order.

2.  Select an order from the list of your orders that you would like to get help for.
3.  Take any of the following additional actions:
    -   Add a comment
    -   Attach a picture
    -   Contact an agent


</td></tr><tr><td id="d242658e318">

**Get help**

</td><td>

If you are an anonymous user not logged into the application, enter keywords for your issue. The chatbot returns a list of related knowledge articles that have been made public. If there are no matching articles that would help resolve the issue, you can choose to be transferred to a live agent.

</td></tr><tr><td id="d242658e340">

**Submit Request**

</td><td>

1.  Initiate submitting your request for one of the catalog items.
    -   If you are using the virtual agent conversation without enabling NLU, click **Show Me Everything** and then click **Submit a request**.
    -   If you are using NLU in your virtual agent conversation, enter an utterance for example open a request, that will identify that there is a NLU and intent associated.
2.  Select the catalog item. The Search Catalog Item topic block searches for the catalog item and displays a link based on your search. For more information about search catalog item, see [ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=itsm-virtual-agent&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)

**Note:** Wherever the topic is opened, the records will display on the same portal.

3.  Click on the link displayed and exit the virtual agent if you do not have any further request.


</td></tr><tr><td id="d242658e389">

**Create Case**

</td><td>

Creates a case from Virtual Agent. You need the following fields to create a case:

-   short\_description \(mandatory\)
-   description
-   account\_sys\_id
-   contact\_sys\_id
-   consumer\_sys\_id
The values of these can be empty. If the account, contact, and consumer fields are empty, the logged in user details are populated. The topic block returns the variable case\_sys\_id from the toic block.

</td></tr><tr><td id="d242658e419">

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

</td></tr><tr><td id="d242658e456">

**Log a complaint**

</td><td>

Select this option to create a complaint case from Virtual Agent. Provide a brief description of the complaint and review the contextual search results. If the results do not provide an answer, enter the following information to create a case:

-   Complaint type
-   Product or location
-   Category and subcategory \(if applicable\)\(
-   Date
-   Complaint details
-   Expected resolution
 After the case is created, you can add a comment to the case or add attachments.

**Note:** This option is available with the [Case Playbook for Complaints](../concept/csm-playbook-complaint-overview.md) application.

</td></tr><tr><td id="d242658e511">

**Request a callback**

</td><td>

Request a callback when the wait time to reach agents is long or agents are unavailable.

</td></tr></tbody>
</table>5.  To exit a chat conversation, click **I'm done**.


**Related topics**  


[Customer Service Virtual Agent conversations](../concept/csm-virtual-agent-chatbot.md)

[Maximizing code reuse with topic blocks](https://www.servicenow.com/docs/access?context=topic-blocks-overview&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

