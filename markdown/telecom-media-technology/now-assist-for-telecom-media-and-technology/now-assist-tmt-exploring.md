---
title: Exploring Now Assist for Telecommunications, Media and Technology \(TMT\)
description: With the Now Assist for Telecommunications, Media and Technology \(TMT\) application, your agents can use generative AI to summarize service problem cases, account onboarding cases, engagements, touchpoints, internal plays, customer plays, successive initiatives, tests, risk signal and issues, and generate resolution notes. Additionally, you can automate transformation mapping between provider and consumer instances in Service Exchange.
locale: en-US
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Exploring Now Assist for Telecommunications, Media and Technology \(TMT\)

With the Now Assist for Telecommunications, Media and Technology \(TMT\) application, your agents can use generative AI to summarize service problem cases, account onboarding cases, engagements, touchpoints, internal plays, customer plays, successive initiatives, tests, risk signal and issues, and generate resolution notes. Additionally, you can automate transformation mapping between provider and consumer instances in Service Exchange.

## Overview of Now Assist for TMT

The following generative AI capabilities are available:

-   **Telecommunications Now Assist capabilities**
    -   A service problem case summary enables an agent to gather the case context on long-running or complex cases. Because these cases can contain several details, including conversation with customers or other agents, generating a summary can help agents to get a quicker understanding of the case.
    -   The case resolution notes can help an agent to wrap up cases faster and provide the context about the case resolution to the other agents who might encounter similar issues.
    -   A test summary assists an agent with obtaining the test results that were generated after executing the test runs. It provides a high-level overview of the test run in a clear format.
    -   Knowledge generation can help an agent to streamline content creation. An agent can automatically generate knowledge articles by using the relevant data from the case record after proposing a resolution or closing the case. By not having to generate knowledge articles manually, this feature can save your agents valuable time and effort.
    -   The customer service summary skill provides you with a concise summary of a sold product, including the current situation, root cause indicators, critical actions, and resolution details.
-   **Technology Now Assist capabilities**
    -   An account onboarding case summary enables an agent to gather case context on onboarding cases. Agents can generate a summary to gain understanding of any stage of the onboarding cycle.
    -   An engagement record summary can enable an agent to summarize initiatives, outcomes, risks, and internal plays associated with an engagement.
    -   A touchpoint record summary can enable an agent to summarize meetings and emails exchanged during the engagement life cycle.
    -   A customer play record summary that includes details of the record and all the associated tasks.
    -   A internal play record summary that includes details of the record and all the associated tasks.
    -   A success initiative record summary that includes details of the record and all the associated tasks.
    -   Collects and analyzes metric data, processes large data sets, identifies patterns and anomalies.
    -   Transform map assist enables providers to automatically generate transform maps between provider and consumer tables.
    -   The risk signal and issues summarization skill provides you with a summary of risk history and resolution context.

## Skills

The Now Assist for TMT application includes the following generative AI skills:

-   **Customer service summary**

    Summarize the service details mentioning the current situation, any critical actions to be taken and find the root cause indicators using the knowledge graph and service summary skill.![Generate service summary.](../image/now-assist-generate-summary.png)


-   **Service Problem Case summarization**

    Generates a summary of a service problem case, including the issue and the actions taken. An agent can generate a summary of a case to understand the case context, refresh the summary so that it includes the latest updates to the case, and post the summary to the case work notes.

    The service problem case summarization skill generates a service problem case summary and displays it below the Case highlights card. The summary includes the information that the agent or customer enters in the following service problem case record fields:

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
    ![Service problem case summary.](../image/serviceproblemcase-summary.png)

-   **Resolution notes generation**

    Generates resolution notes for a service problem case, proposes the resolution to the customer, and adds the information to the service problem case record.![Resolution notes summary.](../image/resolution-notes-summary.png)

-   **Test summarization**

    Generates a test run summary after the test is executed. It includes the main points covered during the test execution, including the test output, test interpretation, and other defined test parameters. An agent can generate a test summary of the executed tests to identify the root cause of the problem.

    ![Test summary.](../image/test-summary.png)

-   **Knowledge generation**

    Generates a knowledge article from a case after proposing a resolution or closing the case.

    The knowledge generation skill displays a pop-up window that an agent can use to generate a knowledge article that is based on similar cases and review it before publishing the knowledge article draft.

    ![knowledge article pop-up window.](../image/serviceproblemcase-knowledge-article.png)

-   **Account onboarding case summarization**

    Summarizes an account onboarding case, including details about each stage in the account onboarding lifecycle. Agents can quickly get up to speed on the status of the onboarding case and case tasks with a high-level summary of key points of information.

    The account onboarding summarization skill generates an onboarding case summary and displays it above the Activities card. The summary includes the information that the agent enters during the following stages of the account onboarding lifecycle:

    -   Initial Setup
    -   Data Capture &amp; Validation
    -   Development &amp; Automation
    -   Testing &amp; Training
    -   Go-live &amp; Post-Support
    ![Account onboarding case summary.](../image/accountonboarding-summary.png)

-   **Engagement summarization**

    Generates the summary for an engagement including preconfigured parameters such as risks, initiatives, outcomes, cases, and internal plays. Customer success managers can quickly get up to speed on all activities and the overall engagement with a high-level summary of the key points of information.

    The engagement summarization skill generates a summary of the engagement including the status, go-live date, renewal date, worknotes, and any outstanding actions and displays it above the Account details card. The summary includes the information that the agent enters in the following engagement record fields:

    -   Title
    -   Description
    -   Work notes
    ![Engagement summary.](../image/engagement-summary.png)

-   **Touchpoint summarization**

    Generates a summary of the different touchpoints in the engagement lifecycle. Customer success managers can get a quick summary of all meetings and emails exchanged between the different stakeholders and any follow up activities.

    The touchpoint summarization skill generates a summary of the touchpoints including the meeting agenda, meeting type, type of meeting, and emails. The summary includes the information that the agent enters in the following touchpoint record fields:

    -   Subject
    -   Description
    -   Work notes
    -   Additional comments
    ![Touchpoint summary.](../image/touchpoint-summary.png)

-   **Transform mapping assist**

    Uses the NOW Large Language Model \(LLM\) to enable Service Exchange providers to automatically generate a transform mapping between provider and consumer tables. This skill enables providers to streamline the transformation mapping process by reducing errors and improving overall efficiency.

-   **Customer play summarization**

    Generates a summary of the customer play and includes the record details and associated customer play tasks.

    The customer play summarization skill generates a summary of the customer play record and highlights critical information such as the number of tasks due in the 7 days or days remaining to close the record. The summary includes the following sections:

    -   Overview
    -   Progress updates
    -   Next steps
    ![Customer play summary](../image/customer-play-summary.jpg)

-   **Internal play summarization**

    Generates a summary of the internal play and includes the record details and associated internal play tasks.

    The internal play summarization skill generates a summary of the internal play record and highlights critical information such as the number of tasks due in the 7 days or days remaining to close the record. The summary includes the following sections:

    -   Overview
    -   Progress updates
    -   Next steps
    ![Internal play summary](../image/internal-play-summary.jpg)

-   **Success initiative summarization**

    Generates a summary of the success initiative and includes the record details and associated success tasks.

    The success initiative summarization skill generates a summary of the success initiative record and highlights relevant critical information. The summary includes the following sections:

    -   Overview
    -   Progress updates
    -   Next steps
    ![Success initiative summary](../image/success-init-summary.jpg)

-   **Analyze metric data trend**

    Collects and analyzes metric data, processes large data sets, identifies patterns and anomalies. Provides clear actionable insights that enables the [Now Assist for Telecommunications, Media and Technology \(TMT\) Monitor engagement health agentic workflow](now-assist-tmt-monitor-health.md) to make informed decisions and take appropriate actions.

-   **Risk signal and issues summarization**

    Generates a summary from a risk signal and issues summarization record, risk solution and risk occurrences.

    The risk signal and issues summarization skill generates a summary of the risk signal and issues record and highlights relevant critical information. The summary includes the following sections:

    -   Overview
    -   Progress update
    -   Next steps
    ![risk signal and issues summarization.](../image/now-assist-risk-signal-issue.png)


## Now Assist panel in CSM/FSM Configurable Workspace

An agent can use the Now Assist panel in CSM/FSM Configurable Workspace.

This conversational interface enables an agent to request a service problem case summary and generate the service problem case resolution notes. For more information about the Now Assist panel, see [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Related topics**  


[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

[Exploring Now Assist Admin](https://www.servicenow.com/docs/access?context=exploring-now-assist-platform&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

