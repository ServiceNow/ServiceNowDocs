---
title: ServiceNow AI agents library
description: All ServiceNow AI agents are listed. Depending on your license, not all AI agents may appear in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-agent-landing-page.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [AI agents and agentic workflows, Enable AI Experiences]
---

# ServiceNow AI agents library

All ServiceNow® AI agents are listed. Depending on your license, not all AI agents may appear in your instance.

## Prerequisites and setup

To access an AI agent, you must have either the appropriate ServiceNow Otto plugins installed or have access to the appropriate pricing tier. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md).

## AI agent role filtering

Each AI agent comes with specific user and data access roles by default. These roles vary with the purpose of each AI agent. You can modify these settings as needed on your instance. If an agent is not performing as expected, it may be due to a roles issue. Either it does not have the appropriate user access, or it does not have the appropriate data access.

AI agents use [role filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/implement-aias-security-new.md) to determine which users can access them. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define access rules for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/define-sec-aia-new.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for the records you want to evaluate for readiness. For example, you can add the itil role to the AI agent's list of approved roles so that it can access Incident records.

## AI agents as users

When a Virtual Agent conversation is triggered, any updates or comments in the record's work notes display as the AI agent rather than the user who initiated the conversation.

## Accessing an AI agent

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Go to the **AI Agents** tab.
3.  Select the name of an agent.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

**Note:** We have controls in place to enable/disable the data collection and data processing.

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. Customers can opt out of future data collection at any time, as described in the [AI Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

