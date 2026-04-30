---
title: General guidelines for using Now Assist for app generation in ServiceNow Studio
description: Learn general guidelines for using Now Assist for app generation to create applications with help from generative AI.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [Explore, Now Assist for app generation in ServiceNow Studio, Working with Now Assist tools and AI files, Use, ServiceNow Studio, Developing your application, Building applications]
---

# General guidelines for using Now Assist for app generation in ServiceNow Studio

Learn general guidelines for using Now Assist for app generation to create applications with help from generative AI.

## Having a conversation

To get the most out of app generation, craft your statements thoughtfully and include details. As Now Assist for app generation makes suggestions and you see the preview, respond and add more details about your requirements.

-   **Initiation**

    Now Assist for app generation asks for the main purpose of your application.

    You can start with a generic statement. For example, `I'd like to manage how my employees travel within my business.`

-   **Conversation**

    Engage in the ongoing process of telling Now Assist how you want your app to work and respond to its inquiries.

    If you know exactly what you want, be direct and specific. For example:

    -   `I want a table for travel requests with fields like employee name, destination, and trip duration.`
    -   `I want employees to be able to create and submit requests. Managers can then view these, and approve or deny them. Employees can view requests they've submitted, but not requests submitted by others.`
    -   `I would like a form for employees to submit requests, and another form for managers to review and respond to those requests.`
    -   `Please add a workspace with a dashboard containing relevant reports about the travel requests.`
    You can also convey only what you know, and collaborate with Now Assist to fill in the gaps. For example:

    -   `I need to collect and monitor relevant data for each employee trip. Can you suggest anything?`

        Now Assist suggests:

        `Sure, we can begin with the basics. How about capturing the employee's name, destination, duration of travel, purpose of travel, and budget. Does that sound like a good starting point?`

    -   `Yes, thanks. I need to manage permissions for my app's users. What can you do for me?`

        Now Assist explains:

        `We can create roles to manage permissions. Can you tell me more about the types of users for your application and what they should be able to do?`

    -   `Sure. Currently, employees email their managers for travel approval, and the manager decides whether the employee gets to go, per budget at the department level.`

        Now Assist clarifies:

        `So, should employees be able to create and view their own requests, and should managers be able to view and approve all requests?`

    -   `That sounds good, thanks.`

        Now Assist understands your workflow and suggests ways to implement the desired functionality:

        `Would you also like to create forms for employees to submit and update travel requests?`

        `Do you want to build a form for managers to approve or reject the travel request?`

        `We could also create a record producer. This will allow employees to submit travel requests directly from the Service Catalog. Would you like to include this feature in your application?`

    Throughout the conversation, Now Assist adjusts its understanding of the application requirements based on your input.


**Parent Topic:**[Exploring Now Assist for app generation in ServiceNow Studio](sns-exploring-now-assist-gen.md)

