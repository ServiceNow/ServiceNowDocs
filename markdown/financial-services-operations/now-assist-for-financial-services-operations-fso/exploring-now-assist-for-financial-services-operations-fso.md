---
title: Exploring Now Assist for Financial Services Operations \(FSO\)
description: With the Now Assist for Financial Services Operations \(FSO\) application, your agent can use generative AI to summarize the case details, understand the case context, and wrap up cases faster.
locale: en-US
release: xanadu
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [generative AI for FSO overview, generative AI for financial service operations overview, generative AI for financial service operations sensitive data handling]
breadcrumb: [Now Assist for Financial Services Operations \(FSO\), Financial Services Operations \(FSO\)]
---

# Exploring Now Assist for Financial Services Operations \(FSO\)

With the Now Assist for Financial Services Operations \(FSO\) application, your agent can use generative AI to summarize the case details, understand the case context, and wrap up cases faster.

## Overview

An agent can generate a case summary for an insurance claim or a card dispute faster with generative AI. Insurance claims and card disputes can contain a lot of information that an agent needs to go through before a case can be successfully resolved. By using an AI-generated case summary, an agent can gather the information that they need, understand the case context, and resolve these cases faster.

## Skills

The Now Assist for Financial Services Operations \(FSO\) includes generative AI skills that enable your agents to understand a case so that they can help resolve cases quickly.

-   **Case summarization**

    Provides an agent with a summary of an insurance claim case or card dispute case, including the issue and the actions taken. An agent can generate a summary of a case to understand the case context. They can refresh the summary so that it includes the latest updates to the case, and post the summary to the case work notes.

    The generated case summary displays in the following areas:

    -   Insurance: Next to the claim details panel in the claim summary page, claim workspace, and claim details page
    -   Banking: Between the activities and case information panel
    The summary includes the information that the agent enters in the case record fields that are listed in the following table.

<table id="table_mgm_bw3_mbc"><thead><tr><th>

Industry

</th><th>

Skill description

</th><th>

Record fields

</th></tr></thead><tbody><tr><td>

Insurance

</td><td>

Provides a customized skill that is configured with a series of related tables for claims cases. The directions address a wide range of claims cases for all lines of business. Summarization is available at the base case level.

</td><td>

-   Incident description
-   Incident location
-   Incident date
-   Nature of loss
-   Stage
-   Assigned to
-   Insurance policy
-   Total claim amount


</td></tr><tr><td>

Banking

</td><td>

Provides a customized skill that is configured with a series of related tables for card dispute cases. The directions cover a range of card dispute cases across various categories.

</td><td>

-   Short description
-   Created
-   Assigned to
-   Stage
-   Dispute amount
-   Card network
-   Category
-   Reason code
-   Consumer
-   Account
-   Service
-   Product


</td></tr></tbody>
</table>
## Now Assist panel in Financial Services Workspace

An agent can use the Now Assist panel in Financial Services Workspace. This conversational interface enables an agent to request a case summary. For more information about the Now Assist panel, see [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Sensitive data handling

Personally identifiable information and other sensitive data can be masked so that it doesn't appear in generative AI prompts. Placeholder text is sent with the prompt instead, and that placeholder text is replaced with the original text after the response has been received. This two-way masking ensures that your users see the correct values, but the Now LLM Service isn't exposed to any sensitive information. For more information, see [Configure sensitive data handling for generative AI](https://www.servicenow.com/docs/access?context=configure-sensitive-data-handling-for-generative-ai&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

**Important:** Exercise caution when using Now Assist for FSO with cases that contain sensitive data or other regulated workloads, such as healthcare claims. Now Assist for FSO should not be used for processing protected health information \(PHI\). When using Now Assist for FSO in a protected industry, validate and test the generated results in accordance with corresponding legislation and requirements. See [AI limitations](now-assist-for-financial-services-operations.md#id_jvg_1wv_lbc) for more information.

