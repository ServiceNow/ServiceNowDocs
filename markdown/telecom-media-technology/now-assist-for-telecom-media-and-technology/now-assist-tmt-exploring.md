---
title: Exploring Now Assist for Telecommunications, Media and Technology \(TMT\)
description: With the Now Assist for Telecommunications, Media and Technology \(TMT\) application, your agents can use generative AI to summarize the service problem case details to create the context of the case faster. In addition, this application will collect case information \(for case summarization\). Your agents can also generate the case resolution notes to share with the other agents and it can help wrap up cases faster.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-exploring.html
release: xanadu
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Now Assist for Telecommunications, Media and Technology \(TMT\), Telecommunications, Media, and Technology]
---

# Exploring Now Assist for Telecommunications, Media and Technology \(TMT\)

With the Now Assist for Telecommunications, Media and Technology \(TMT\) application, your agents can use generative AI to summarize the service problem case details to create the context of the case faster. In addition, this application will collect case information \(for case summarization\). Your agents can also generate the case resolution notes to share with the other agents and it can help wrap up cases faster.

## Now Assist for Telecommunications, Media and Technology \(TMT\) overview

The following generative AI capabilities are available for an agent:

-   A service problem case summary enables an agent to gather the case context on long-running or complex cases. Because these cases can contain a lot of information, including the conversations with the customer or other agents, an agent can generate a summary to gain understanding faster.
-   The case resolution notes can help an agent to wrap up cases faster and provide the context about the case resolution to the other agents who might encounter similar issues.
-   A test summary assists an agent with obtaining the test results that were generated after executing the test runs. It provides a high-level overview of the test run in a clear format.

## Skills

The Now Assist for TMT application includes the generative AI skills that enable your agents to understand the service problem case context so that they can propose resolutions to the customer more quickly.

-   **Service Problem Case summarization**

    Provides an agent with a summary of a service problem case, including the issue and the actions taken. An agent can generate a summary of a case to understand the case context, refresh the summary so that it includes the latest updates to the case, and post the summary to the case work notes.

    The service problem case summarization skill generates a service problem case summary and displays it below the Case highlights card. The summary includes the information that the agent or customer enters in the following service problem case record fields:

    -   Short description
    -   Description
    -   Work notes
    -   Additional comments
    \[Omitted image "serviceproblemcase-summary.png"\] Alt text: Service problem case summary

-   **Resolution notes generation**

    Enables an agent to generate the resolution notes for a service problem case, propose the resolution to the customer, and add the information to the service problem case record.

    The resolution notes generation skill displays a pop-up window that an agent can use to select a resolution code and review the resolution notes text before proposing a resolution to a customer.

    **Note:** The resolution notes generation skill requires a minimum of 50 words in the case record to generate the resolution notes. If the resolution notes can't be generated, the system displays a message below the Resolution notes field.

    \[Omitted image "resolution-notes-summary.png"\] Alt text: Resolution notes summary

-   **Test summarization**

    Provides an agent with a test run summary after the test is executed. It includes the main points covered during the test execution, including the test output, test interpretation, and other defined test parameters. An agent can generate a test summary of the executed tests to identify the root cause of the problem.


## Now Assist panel in CSM/FSM Configurable Workspace

An agent can use the Now Assist panel in CSM/FSM Configurable Workspace. This conversational interface enables an agent to request a service problem case summary and generate the service problem case resolution notes. For more information about the Now Assist panel, see [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/intelligent-experiences/enable-ai-experiences/now-assist-panel-overview.md).

\[Omitted image "test-summary.png"\] Alt text: Test summary.

**Related topics**  


[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/intelligent-experiences/enable-ai-experiences/platform-now-assist-landing.md)

[Exploring Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/intelligent-experiences/enable-ai-experiences/exploring-now-assist-platform.md)

