---
title: Virtual Agent for Universal Request
description: The Virtual Agent capabilities of Universal Request provide automated chat options to employees. It reduces the workload of agents by assisting the requester with certain basic tasks. It can display suggestions for self-help topics and knowledge articles based on keywords. It can also help employees to update their universal requests.
locale: en-US
release: yokohama
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Universal Request, Employee Service Management]
---

# Virtual Agent for Universal Request

The Virtual Agent capabilities of Universal Request provide automated chat options to employees. It reduces the workload of agents by assisting the requester with certain basic tasks. It can display suggestions for self-help topics and knowledge articles based on keywords. It can also help employees to update their universal requests.

The Virtual Agent capabilities of Universal Request can help your employees do the following:

-   Create a universal request.
-   Mark a universal request as sensitive while creating it.
-   Track universal requests opened for them.
-   Add comments to universal requests opened for them.
-   Update the watchlist for universal requests opened for them.
-   Close universal requests opened for them.

Virtual Agent uses predefined topic conversations to interact with employees. The information exchanged during the conversation flow, such as user inputs and virtual agent responses, enables the virtual agent to fulfill a request or help complete a task. The conversation topics available by default with Universal Request are as follows:

-   The Employee Help Request topic enables employees to create universal requests using the Virtual Agent. When a request contain sensitive information, the Virtual Agent marks the request as sensitive after confirming with the employee. If your organization uses the ServiceNow® Predictive Intelligence solution, you can train the solution to detect sensitive information on its own. Predictive Intelligence can also predict the correct department for the primary ticket of the universal request. Using Predictive Intelligence, the employee can now create a ticket and assign it to the correct department.
-   The Track Universal Request Status topic enables users to track and update the universal requests opened for them. Employees can add comments or update the watchlist of their request. They can also close a ticket after providing a reason. The topic has an integrated NLU model, enabling requesters to enter their queries in natural language utterances. Some of the utterances include the following queries:
    -   Track my request
    -   Track my ticket
    -   What is the status of my request
    -   Need an update on my ticket

These topic conversations are available in all supported Universal Request Virtual Agent messaging integrations.

-   **[Create a universal request using Virtual Agent](../task/ur-create-ur-using-va.md)**  
Create a universal request with the help of Virtual Agent. You can access the Virtual Agent using the chat option in the search page of Service Portal.
-   **[Update or cancel a universal request using Virtual Agent](../task/ur-cancel-ur-using-va.md)**  
Update or cancel a universal request with the help of the Virtual Agent in the chat option.
-   **[Universal Request Virtual Agent conversation flows](ur-va-conversation-flows.md)**  
Universal Request Virtual Agent includes several predefined topic conversations that you can use to resolve common tasks on your universal requests.

**Parent Topic:**[Universal Request](ur-landing-limitedaccess.md)

