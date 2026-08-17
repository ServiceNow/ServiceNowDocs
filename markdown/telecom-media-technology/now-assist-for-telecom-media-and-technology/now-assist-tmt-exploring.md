---
title: Exploring ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)
description: With the ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) application, your agents can use generative AI to summarize service problem cases, account onboarding cases, engagements, touchpoints, and internal plays. Agents can also summarize customer plays, successive initiatives, tests, risk signals, and issues, and generate resolution notes. Additionally, you can automate transformation mapping between provider and consumer instances in Service Exchange.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-exploring.html
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\), Telecommunications, Media, and Technology \(TMT\)]
---

# Exploring ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)

With the ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) application, your agents can use generative AI to summarize service problem cases, account onboarding cases, engagements, touchpoints, and internal plays. Agents can also summarize customer plays, successive initiatives, tests, risk signals, and issues, and generate resolution notes. Additionally, you can automate transformation mapping between provider and consumer instances in Service Exchange.

## Overview of ServiceNow Otto for TMT

The following generative AI capabilities are available:

-   **Telecommunications ServiceNow Otto capabilities**
    -   The Telecom Customer 360 insights generation automatically generates AI-powered insights for a customer or consumer account.
    -   A service problem case sentiment analysis enables you to understand the customer sentiment on a service problem case.
    -   A comprehensive summary of linked records enables you to generate a summary of linked records of an escalated complaint in the Alternative Dispute Resolution \(ADR\) case.
    -   A deadlock letter draft generation enables you to generate the deadlock letter for an ADR case. If the customer rejects the resolution plan, you can share the deadlock letter with the customer.
    -   A resolution notes generation enables the agent to create a resolution plan for an escalated complaint in the ADR case record.
    -   A service problem case summary enables an agent to gather the case context on long-running or complex cases. Because these cases can contain several details, including conversation with customers or other agents, generating a summary can help agents to get a quicker understanding of the case.
    -   The case resolution notes can help an agent to wrap up cases faster. They provide context about the case resolution to other agents who might encounter similar issues.
    -   A test summary assists an agent with obtaining the test results that were generated after executing the test runs. It provides a high-level overview of the test run in a clear format.
    -   Knowledge generation can help an agent to streamline content creation. An agent can automatically generate knowledge articles by using the relevant data from the case record after proposing a resolution or closing the case. By not having to generate knowledge articles manually, this feature can save your agents valuable time and effort.
    -   The customer service summary skill provides you with a concise summary of a sold product, including the current situation, root cause indicators, critical actions, and resolution details.
    -   Remote Hands Agents can generate a case summary from both the Remote Hands Case table and the CSM/FSM Configurable Workspace using the Summarize option. The summary provides a consolidated overview of the case, including key case details and related case summary for quick understanding.
-   **Technology ServiceNow Otto capabilities**
    -   Draft closure notes for risk signals automatically generate and close eligible signals daily based on their associated risk solution status.
    -   A lookup similar engagements skill to automatically generate a product adoption roadmap based on engagement data and insights from similar engagements.
    -   A renewal insight engine skill to analyze the renewal likelihood and expansion potential of an engagement or contract and generate recommended actions.
    -   An account onboarding case summary enables an agent to gather case context on onboarding cases. Agents can generate a summary to gain an understanding of any stage of the onboarding cycle.
    -   An engagement record summary can enable an agent to summarize initiatives, outcomes, risks, and internal plays associated with an engagement.
    -   A touchpoint record summary can enable an agent to summarize meetings and emails exchanged during the engagement life cycle.
    -   A customer play record summary that includes details of the record and all the associated tasks.
    -   A internal play record summary that includes details of the record and all the associated tasks.
    -   A success initiative record summary that includes details of the record and all the associated tasks.
    -   Collects and analyzes metric data, processes large data sets, identifies patterns and anomalies.
    -   Transform map assist enables providers to automatically generate transform maps between provider and consumer tables.
    -   The risk signal and issues summarization skill provides you with a summary of risk history and resolution context.

## Skills

The ServiceNow Otto for TMT application includes the following generative AI skills:

-   **Service Problem Case sentiment analysis**

    Sentiment analysis helps agents to identify the most current sentiment on the service problem cases. This skill enables you to select the relevant linked records for ADR case record.


-   **Comprehensive Summary of Linked Records**

    The comprehensive summary of linked records skill summarizes the details of the case records that are linked to an escalated complaint in an ADR case. The comprehensive summary includes the following sections:

    -   Chronological sequence of events
    -   Identified findings
    -   Resolution steps completed
    -   Outstanding gaps
    -   Recommended direction

-   **Deadlock letter draft generation**

    The deadlock letter draft generation skill creates the deadlock letter for a customer complaint. You can generate the deadlock letter when the customer rejects the complaint resolution and opt for legal procedures. The deadlock letter draft includes the following sections:

    -   Summary of Your Complaint
    -   Our Investigation and Response
    -   Chronological sequence of events
    -   Identified findings
    -   Resolution steps completed

-   **Resolution notes generation for ADR**

    The resolution notes generation skill creates the resolution notes for an escalated customer complaint in the ADR case record. The resolution notes generation includes the following sections:

    -   Issue
    -   Cause
    -   Resolution steps

-   **Customer service summary**

    Summarize the service details mentioning the current situation, any critical actions to be taken and find the root cause indicators using the knowledge graph and service summary skill.


-   **Service Problem Case summarization**

    Generates a summary of a service problem case, including the issue and the actions taken. An agent can generate a summary of a case to understand the case context. The agent can refresh the summary to include the latest updates and post the summary to the case work notes.

    The service problem case summarization skill generates a service problem case summary and displays it previous the Case highlights card. The summary includes the information that the agent or customer enters in the following service problem case record fields:

    -   Short description
    -   Description
    -   Work notes
    -   Additional comments
    -   Diagnostic Task

        Fields:

        -   Description
        -   Short description
        -   Work notes
        -   state
        -   sys id
    -   Resolution Task

        Fields:

        -   Description
        -   Short description
        -   Work notes
        -   state
-   **Resolution notes generation**

    Generates resolution notes for a service problem case, proposes the resolution to the customer, and adds the information to the service problem case record.

-   **Test summarization**

    Generates a test run summary after the test is executed. It includes the main points covered during the test execution, including the test output, test interpretation, and other defined test parameters. An agent can generate a test summary of the executed tests to identify the root cause of the problem.

-   **Knowledge generation**

    Generates a knowledge article from a case after proposing a resolution or closing the case.

    The knowledge generation skill displays a pop-up window that an agent can use to generate a knowledge article based on similar cases. Agents can review the draft before publishing.

-   **Account onboarding case summarization**

    Summarizes an account onboarding case, including details about each stage in the account onboarding lifecycle. Agents can quickly get up to speed on the status of the onboarding case and case tasks with a high-level summary of key points of information.

    The account onboarding summarization skill generates an onboarding case summary and displays it before the Activities card. The summary includes the information that the agent enters during the following stages of the account onboarding lifecycle:

    -   Initial Setup
    -   Data Capture &amp; Validation
    -   Development &amp; Automation
    -   Testing &amp; Training
    -   Go-live &amp; Post-Support
-   **Engagement summarization**

    Generates the summary for an engagement including preconfigured parameters such as risks, initiatives, outcomes, cases, and internal plays. Customer success managers can quickly get up to speed on all activities and the overall engagement with a high-level summary of the key points of information.

    The engagement summarization skill generates a summary of the engagement including the status, go-live date, renewal date, worknotes, and any outstanding actions and displays it before the Account details card. The summary includes the information that the agent enters in the following engagement record fields:

    -   Title
    -   Description
    -   Work notes
-   **Touchpoint summarization**

    Generates a summary of the different touchpoints in the engagement lifecycle. Customer success managers can get a quick summary of all meetings and emails exchanged between the different stakeholders and any follow up activities.

    The touchpoint summarization skill generates a summary of the touchpoints including the meeting agenda, meeting type, type of meeting, and emails. The summary includes the information that the agent enters in the following touchpoint record fields:

    -   Subject
    -   Description
    -   Work notes
    -   Additional comments
-   **Transform mapping assist**

    Uses the NOW Large language model \(LLM\) to enable Service Exchange providers to automatically generate a transform mapping between provider and consumer tables. This skill enables providers to streamline the transformation mapping process by reducing errors and improving overall efficiency.

-   **Customer play summarization**

    Generates a summary of the customer play and includes the record details and associated customer play tasks.

    The customer play summarization skill generates a summary of the customer play record and highlights critical information such as the number of tasks due in the 7 days or days remaining to close the record. The summary includes the following sections:

    -   Overview
    -   Progress updates
    -   Next steps
-   **Internal play summarization**

    Generates a summary of the internal play and includes the record details and associated internal play tasks.

    The internal play summarization skill generates a summary of the internal play record and highlights critical information such as the number of tasks due in the 7 days or days remaining to close the record. The summary includes the following sections:

    -   Overview
    -   Progress updates
    -   Next steps
-   **Success initiative summarization**

    Generates a summary of the success initiative and includes the record details and associated success tasks.

    The success initiative summarization skill generates a summary of the success initiative record and highlights relevant critical information. The summary includes the following sections:

    -   Overview
    -   Progress updates
    -   Next steps
-   **Analyze metric data trend**

    Collects and analyzes metric data, processes large data sets, identifies patterns and anomalies. Provides clear actionable insights that enables the [ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) monitor engagement health agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-monitor-health.md) to make informed decisions and take appropriate actions.

-   **Risk signal and issues summarization**

    Generates a summary from a risk signal and issues summarization record, risk solution and risk occurrences.

    The risk signal and issues summarization skill generates a summary of the risk signal and issues record and highlights relevant critical information. The summary includes the following sections:

    -   Overview
    -   Progress update
    -   Next steps

## ServiceNow Otto panel in CSM/FSM Configurable Workspace

An agent can use the ServiceNow Otto panel in CSM/FSM Configurable Workspace.

This conversational interface enables an agent to request a service problem case summary and generate the service problem case resolution notes. For more information about the ServiceNow Otto panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md).

## ServiceNow Otto in Remote Hands Request management application

Remote Hands Request Summarization is an ServiceNow Otto capability that provides a contextual overview of a Remote Hands case. It combines current case data with insights from similar historical cases. Users with the Remote Hands Agent role can generate a summarized view of a Remote Hands case. Select the **Summarize** option from either the Remote Hands Case table or the CSM/FSM Configurable Workspace.

The comprehensive summary includes the following sections:

-   Case Overview: The Case Overview section displays the key metadata retrieved from the Remote Hands Case table, including Case Category, Priority, Channel, and State.
-   Case Details: The Case Details section displays the Short Description and Description fields from the Remote Hands case record, providing detailed context about the current request
-   Related Case Summary: The Related Case Summary section is generated based on similar cases existing in the Remote Hands Case table.
-   Case Reference: The Case Reference lists up to five similar cases found by the system
-   Case Issue: The Case Issue displays the Short Description of the related case
-   Case Resolution: The Case Resolution displays the Resolution Notes recorded in the related case

**Related topics**  


[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)

[Exploring AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-now-assist-platform.md)

