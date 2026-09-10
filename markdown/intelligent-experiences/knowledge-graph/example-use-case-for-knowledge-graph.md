---
title: Knowledge Graph integration with ServiceNow Otto for Virtual Agent and ServiceNow Otto panel
description: Knowledge Graph integrates with ServiceNow Otto for Virtual Agent and ServiceNow Otto panel to provide personalized, permission-aware responses based on user context, relationships, and enterprise data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/knowledge-graph/example-use-case-for-knowledge-graph.html
release: australia
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Exploring Knowledge Graph, Knowledge Graph, Enable AI experiences]
---

# Knowledge Graph integration with ServiceNow Otto for Virtual Agent and ServiceNow Otto panel

Knowledge Graph integrates with ServiceNow® Otto for Virtual Agent and ServiceNow Otto® panel to provide personalized, permission-aware responses based on user context, relationships, and enterprise data.

In this release, the available prebuilt integrations with ServiceNow® Otto for Virtual Agent and ServiceNow Otto® panel are:

-   Integration with ServiceNow Otto® for Slot filling: Helps requester and fulfiller in pre-filling the slots for LLM topics and skills execution using Natural Language Querying of Knowledge Graph.
-   Integration with ServiceNow Otto® for User Context: Helps requester and fulfiller with personalized responses.
-   Integration with ServiceNow Otto® for Natural Language Query graph: Helps requester and fulfiller with personalized responses on people queries and Natural Language queries. Also supports people citation card.

**Note:** To enable Knowledge Graph for ServiceNow® Otto for Virtual Agent, ensure that **sn\_vad\_genai.knowledge\_graph.enabled** and **sn\_ais\_assist.enable\_knowledge\_graph\_nlq** system properties are set to true. See [Add a Knowledge Graph schema to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/add-kg-schema-assistant.md).

For more information see [Add a Knowledge Graph schema to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/add-kg-schema-assistant.md).

**Note:**

-   To enable Knowledge Graph functionality in the ServiceNow® Otto for Virtual Agent and conversational catalog, make sure to fill the Slot Filling Schema.
-   To use Knowledge Graph for Question Answering from VA, fill out the Natural Language Query Schema in the ServiceNow Otto® panel.
-   You can only have one active Knowledge Graph schema at a time for either Slot Filling or Natural Language Query. Multiple active Knowledge Graph schemas aren't supported.

## Integration with ServiceNow Otto® for User Context

For the users of ServiceNow Otto®, Knowledge Graph integrates the context from the prebuilt User profile schemas that provide personalized responses.

By leveraging relationships between users, teams, and content, products like AI Search and ServiceNow Otto® can provide relevant, permission-aware answers instead of generic results.

With Knowledge Graph, responses are dynamically tailored based on:

-   Who the user is: Role, department, and location
-   Who they collaborate with: Manager, reportee
-   What assets do they have

Here’s an example use case:

-   An employee uses ServiceNow® Otto for Virtual Agent for information on parental leave policy. They enter the query in the Virtual Agent window `What is my parental leave policy?`
-   Virtual Agent receives the user information like. The employee is based in the country: USA, state: California, City: Santa Clara, from the Knowledge Graph User Profile Schema.
-   This additional user profile context is used to personalize the synthesized response to the exact location of the employee
-   Therefore, instead of getting a link to the parental leave policy document or a generic response, the employee gets a tailored contextualized answer:

    `Your company offers a generous parental leave policy to its employees in California. As of January 2022, the company increased paid time off for workers who give birth to a maximum of 24 weeks from the previous 18. In addition to the company's internal policies, California state law provides further protections. The California Family Rights Act (CFRA) offers eligible employees up to 12 weeks of unpaid, job-protected leave to care for their own serious health condition or that of a family member, or to bond with a new child. This is complemented by the Pregnancy Disability Leave (PDL) law, which provides up to four months of unpaid, job-protected leave for employees disabled by pregnancy, childbirth, or related medical conditions.`


## Integration with ServiceNow Otto® for Slot filling

Knowledge Graph enhances the ServiceNow Otto® user experience and makes the process seamless and efficient by reducing the slot-ﬁlling questions asked during conversations.

Here’s an example use case:

An employee uses ServiceNow Otto® to request a laptop replacement. ServiceNow Otto® uses the assigned Knowledge Graph schema to find information and resolve the query with minimal user inputs.

\[Omitted image "mmasset0020508-knowledgegraph-vertical.svg"\] Alt text: Knowledge Graph example.

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

## Integration with ServiceNow Otto® for natural language queries

Knowledge Graph assist in answering natural language queries accurately. For more examples, see [Natural language queries use cases and examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/natural-language-queries-example-usecases.md)

ServiceNow Otto® can now provide users with information about people in your organization.

If you ask Virtual Agent about a person,the Information about that person you're searching for appears in the synthesized response, along with an inline people citation.

Inline citations appear at the end of the relevant synthesized response sentence. Selecting an inline citation results in a popover containing either a link to an article or source, or a description and action to start the action.

**Note:** Shared files only appear if Knowledge Graph admin has activated the **sn\_kg\_conn\_user\_shared\_files** record in Knowledge Graph related data map \[sn\_kg\_related\_data\_map\_list\] table. To active it, set the **Active** field to **True**.

Here's an example:

\[Omitted image "people-search-example.png"\] Alt text: People results appear in the synthesized response on the portal's search results page and provide details such as the person's name, position, location, and email.

\[Omitted image "people-citation-kg.png"\] Alt text: People results appear in the synthesized response and provide details such as the person's name, position, location, and email.

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
    -   If you have not configured Microsoft OneDrive application, see [Configure Microsoft OneDrive application for Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/create-microsoft-onedrive-app.md).
    \[Omitted image "people-citation-window-kg.png"\] Alt text: Shared files in people citation card


## Integration with AI Search

Knowledge Graph is also integrated with AI Search. You can enable ServiceNow Otto® Multi-Content Response Genius Results to get answers from Knowledge Graph on AI Search.

Ensure that you have already configured Knowledge Graph with an assistant before enabling it on AI search.

To configure and enable the AI Search see [Knowledge base articles Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/now-assist-qna-genius-results.md).

