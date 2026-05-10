---
title: Leverage Knowledge Graph prebuilt integration with Now Assist Virtual Agent and Now Assist Panel
description: The prebuilt integrations of Knowledge Graph can help ServiceNow users to drive productivity, enhance decision-making, and unlock the full potential of enterprise data- while maintaining robust data governance and permission controls.
locale: en-US
release: australia
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Exploring Knowledge Graph, Knowledge Graph, Enable AI experiences]
---

# Leverage Knowledge Graph prebuilt integration with Now Assist Virtual Agent and Now Assist Panel

The prebuilt integrations of Knowledge Graph can help ServiceNow users to drive productivity, enhance decision-making, and unlock the full potential of enterprise data- while maintaining robust data governance and permission controls.

In this release, the available prebuilt integrations with Now Assist Virtual Agent and Now Assist Panel are:

1.  Integration with Now Assist for User Context: Helps requesters and fulfillers with personalized responses.
2.  Integration with Now Assist for Slot filling: Helps requesters and fulfillers in pre-filling the slots for LLM topics and skills execution using Natural Language Querying of Knowledge Graph.
3.  Integration with Now Assist for Natural Language Query graph: Helps requesters and fulfillers with personalized responses on people queries and Natural Language queries. Also supports people citation card.

**Note:** To enable Knowledge Graph for Now Assist Virtual Agent, ensure that **sn\_vad\_genai.knowledge\_graph.enabled** and **sn\_ais\_assist.enable\_knowledge\_graph\_nlq** system properties are set to true. See [Add a Knowledge Graph schema to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/add-kg-schema-assistant.md).

For more information see [Add a Knowledge Graph schema to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/add-kg-schema-assistant.md).

**Note:**

-   To enable Knowledge Graph functionality in the Now Assist Virtual Agent and conversational catalog, make sure to fill the Slot Filling Schema.
-   To use Knowledge Graph for Question Answering from VA, fill out the Natural Language Query Schema in the Now Assist Panel.
-   You can only have one active Knowledge Graph schema at a time for either Slot Filling or Natural Language Query. Multiple active Knowledge Graph schemas are not supported.

## Integration with Now Assist for User Context

For the users of Now Assist, Knowledge Graph integrates the context from the prebuilt User Profile Schemas that provide personalized responses.

By leveraging relationships between users, teams, and content, products like AI Search and Now Assist can provide relevant, permission-aware answers instead of generic results.

With Knowledge Graph, responses are dynamically tailored based on:

-   Who the user is: Role, department, and location
-   Who they collaborate with: Manager, reportee
-   What assets do they have

Here’s an example use case:

-   An employee uses Now Assist Virtual Agent for information on parental leave policy. They enter the query in the Virtual Agent window `What is my parental leave policy?`
-   Virtual Agent receives the user information like. The employee is based in the country: USA, state: California, City: Santa Clara, from the Knowledge Graph User Profile Schema.
-   This additional user profile context is used to personalize the synthesized response to the exact location of the employee
-   Therefore, instead of getting a link to the parental leave policy document or a generic response, the employee gets a tailored contextualized answer:

    `Your company offers a generous parental leave policy to its employees in California. As of January 2022, the company increased paid time off for workers who give birth to a maximum of 24 weeks from the previous 18. In addition to the company's internal policies, California state law provides further protections. The California Family Rights Act (CFRA) offers eligible employees up to 12 weeks of unpaid, job-protected leave to care for their own serious health condition or that of a family member, or to bond with a new child. This is complemented by the Pregnancy Disability Leave (PDL) law, which provides up to four months of unpaid, job-protected leave for employees disabled by pregnancy, childbirth, or related medical conditions.`


## Integration with Now Assist for Slot filling

Knowledge Graph enhances the Now Assist user experience and makes the process seamless and efficient by reducing the slot-ﬁlling questions asked during conversations.

Here’s an example use case:

An employee uses Virtual Agent to request a laptop replacement. Virtual Agent uses the assigned Knowledge Graph schema to find information and resolve the query with minimal user inputs.

![Knowledge Graph example.](../Images/mmasset0020508-knowledgegraph-vertical.svg)

1.  The user uses Virtual Agent to query `Need assistance in laptop replacement.`
2.  Virtual Agent processes the query and generates the following prompts required for this request:
    -   Topic: New laptop request
    -   Name
    -   Location
    -   Department
    -   Laptop model
    -   Address
3.  Virtual Agent first tries to gather this information using Knowledge Graph.
4.  The Knowledge Graph schema leverages LLM to retrieve the data from all the relevant entities, called nodes using the relationship between these nodes, called edges, and provides the following output:
    -   Topic: New laptop request
    -   Name: John Doe
    -   Location: Santa Clara
    -   Department: Marketing
    -   Badge Template: User input needed
    -   Address: 123 Street, CA, USA
5.  Virtual Agent requests verification of the output and add details for the missing fields.
6.  The user can edit and verify the provided information before confirming. Once confirmed, the request is processed with minimal effort from the user.
7.  Virtual Agent processes the user input and completes the user query.

Knowledge Graph leverages the existing information available in the internal databases and auto-populates it to reduce the efforts while making the entire experience seamless.

## Integration with Now Assist for natural language queries

Knowledge Graph assist in answering natural language queries accurately. For more examples, see [Natural language queries use cases and examples](natural-language-queries-example-usecases.md)

Now Assist can now provide users with information about people in your organization.

If you ask Virtual Agent about a person,the Information about that person you're searching for appears in the synthesized response, along with an inline people citation.

Inline citations appear at the end of the relevant synthesized response sentence. Selecting an inline citation results in a popover containing either a link to an article or source, or a description and action to start the action.

**Note:** Shared files only appear if Knowledge Graph admin has activated the **sn\_kg\_conn\_user\_shared\_files** record in Knowledge Graph related data map \[sn\_kg\_related\_data\_map\_list\] table. To active it, set the **Active** field to **True**.

Here's an example:

![People results appear in the synthesized response on the portal's search results page and provide details such as the person's name, position, location, and email.](../Images/people-search-example.png "Example of synthesized response for people on the portal's search results page")

![People results appear in the synthesized response and provide details such as the person's name, position, location, and email.](../Images/people-citation-kg.png "Example of synthesized response with people inline citations in chat")

Selecting the person's name presents a popover. The information in the popover can include the following information:

-   Manager
-   Location
-   Email
-   Teams
-   Phone
-   Shared files

    **Important:**

    -   Shared Microsoft SharePoint files between you and the person found, appear only on the people popover.
    -   The shared files only appear after you have completed the prompt to **Log in**, and signed in successfully. If you do not have a valid token, you will be prompted to sign in and re-directed to Microsoft login page.
    -   If you have not configured Microsoft OneDrive application, see [Configure Microsoft OneDrive application for Knowledge Graph](../Task/create-microsoft-onedrive-app.md).
    ![Shared files in people citation card](../Images/people-citation-window-kg.png)


## Integration with AI Search

Knowledge Graph is also integrated with AI Search. You can enable Now Assist Multi-Content Response Genius Results to get answers from Knowledge Graph on AI Search.

Ensure that you have already configured Knowledge Graph with an assistant before enabling it on AI search.

To configure and enable the AI Search see [Now Assist Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/now-assist-qna-genius-results.md).

