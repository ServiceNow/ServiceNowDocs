---
title: Retrieve Vulnerability and exposure data with generative AI
description: Chat with an AI agent to get help with your questions about Vulnerability Response host and Application Vulnerability Response findings \(vulnerable items and application vulnerable items\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/retrieve-vr-data.html
release: zurich
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 3
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Retrieve Vulnerability and exposure data with generative AI

Chat with an AI agent to get help with your questions about Vulnerability Response host and Application Vulnerability Response findings \(vulnerable items and application vulnerable items\).

## Before you begin

To view and use the generative AI skills agentic workflows in the Unified Security Exposure Management you must upgrade to Unified Security Exposure Management. See [Unified Security Exposure Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/release-notes/secops-sem-rn.md) for more information.

The Now Assist panel must be activated. For more information, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/activate-now-assist-panel.md).

Roles required:

-   sn\_vul.remediation\_owner \(host vulnerable items \(VITs\)\)
-   sn\_vul.vulnerability\_analyst \(host vulnerable items \(VITs\)\)
-   sn\_vul.app\_sec\_manager \(application vulnerable items \(AVITs\)\)

## Procedure

1.  Log into your ServiceNow AI Platform instance.

    The vulnerability records that you can see depend on the roles you have been assigned. Host Vulnerability Response and Application Vulnerability Response findings \(VITs, AVITs\) are supported.

    **Note:**

    You aren't required to have all of these roles assigned to chat with the AI agent. At a minimum, you must have either sn\_vul.remediation\_owner or sn\_vul.vulnerability\_analyst to view VITs. At a minimum, you must have sn\_vul.app\_sec\_manager assigned to view AVITs.

2.  Alternatively, navigate to **Workspaces** in your ServiceNow AI Platform instance and choose one.

<table id="table_a5v_djj_shc"><thead><tr><th>

Option

</th><th>

ServiceNow AI Platform Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**IT Remediation Workspace**

</td><td>

sn\_vul.remediation\_owner for VITs.

</td><td>

The IT Remediation owner \(legacy\) workspace is supported by versions of Vulnerability Response earlier than version 30.0.

</td></tr><tr><td>

**Vulnerability Manager Workspace**

</td><td>

sn\_vul.vulnerability\_analyst for VITs or sn\_vul.app\_sec\_manager for AVITs.

</td><td>

The Vulnerability Manager \(legacy\) workspace is supported by versions of Vulnerability Response earlier than version 30.0.

</td></tr><tr><td>

**Security Exposure Management Workspace**

</td><td>

-   sn\_vul.remediation\_owner \(host vulnerable items \(VITs\)\)
-   sn\_vul.vulnerability\_analyst \(host vulnerable items \(VITs\)\)
-   sn\_vul.app\_sec\_manager \(application vulnerable items \(AVITs\)\)


</td><td>

The Security Exposure Management Workspace is supported by Unified Security Exposure Management \(USEM\). You must have version 30.0 or later of Vulnerability Response installed to view this workspace. See [Implementing Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/configuring-security-exposure-management.md) for more information.

</td></tr></tbody>
</table>3.  In the Now Assist panel, enter your queries in natural language to start a conversation with the AI agent.

    **Note:**

    -   This AI agent is designed to help you answer query-related questions about data for Vulnerability Response and Application Vulnerability Response findings.
    -   Prompts that involve any sort of data analysis of the vulnerability data that might match your questions are not supported by this AI agent.
    -   The AI agent searches for the vulnerability data that matches your question, retrieves it, and creates responses for you based on the data available.
    -   You might prefer to provide as much detail as you can for your questions to help the AI agent.

        For example, as a remediation owner, if you ask the agent a general question such as, **Retrieve all the vulnerable items with scores 5 or greater**, the AI agent's response might be, `No vulnerable items with scores 5 or greater were found. You may want to rephrase your question or adjust your criteria.`

        On findings records, there are multiple fields that might be populated by numeric values such as Risk rating, Risk score, Common Vulnerability Scoring System \(CVSS\), and Exploit Prediction Scoring System \(EPSS\). Given the request for this example, the AI agent won't know which field you want unless you specify the field or provide more details. You can help the AI agent by being specific and rephrasing your question to something like, **Show me all the open VITs with Risk rating 1 - Critical**.

    -   As long as you do not close the conversation, the AI agent uses the context of the conversation for its next response. Select the plus icon \(\[Omitted image "dlp-plus-icon.png"\] Alt text: Icon that indicates you can start a new chat\) to start a new chat.
    -   Be sure to check the answers for accuracy.
4.  Enter follow up questions as needed.

    See [Sample queries for the Retrieve Vulnerability Response data agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/now-assist-vr-retrieve-qbank.md) for a list of sample questions to help you get started.


**Parent Topic:**[Using Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/using-unified-security-exposure-management.md)

