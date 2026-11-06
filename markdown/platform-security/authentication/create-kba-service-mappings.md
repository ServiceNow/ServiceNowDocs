---
title: Specify knowledge-based questions for an AI voice agent service
description: Specify the questions used for caller identification and authentication with a specific AI voice agent service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/create-kba-service-mappings.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure KBA, Knowledge-based authentication, Authentication factor configuration for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Specify knowledge-based questions for an AI voice agent service

Specify the questions used for caller identification and authentication with a specific AI voice agent service.

## Before you begin

Role required: auth\_factors\_admin

Service mappings are created automatically when KBA questions are selected in AI Voice Assistant Designer. You can also create and manage mappings directly in this table. Changes made here are reflected on the Caller Verification screen in Assistant Designer instantly. To learn more about voice services and how to create and manage them, see [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-an-ai-voice-service.md).

## Procedure

1.  Navigate to **All** &gt; **Authentication Factors** &gt; **Knowledge Based Factor** &gt; **Question Service Mappings**.

2.  Select **New** on the Knowledge Based Question Service Mappings page.

3.  Specify the following fields on the form.

<table id="table_gtp_xb1_jhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Profile Table

</td><td>

Table for your service.

</td></tr><tr><td>

Application

</td><td>

Global application scope is selected by default.

</td></tr><tr><td>

Service Profile

</td><td>

Service profile for the mapping. Example: Choosing a voice agent: **Voice Deployment - Example**.

</td></tr><tr><td>

Question

</td><td>

Question to assign to this service mapping.**Note:** A validation error is returned for the following:

-   The selected question must have a corresponding question-answer mapping configured. If it does not, the question is cleared and a validation error is returned.
-   When a question with Type = **Authentication** is assigned a Service mapping with Type = **Identification**, the mapping action is aborted with an error message and a validation error is returned.


</td></tr><tr><td>

Type

</td><td>

Type of service mapping to use. Options:-   **Authentication**: The question is used during the authentication phase.
-   **Identification**: The question is used during the identification phase.


</td></tr><tr><td>

Usage

</td><td>

Available when Type is set to **Identification**. Role of this question in the identification flow. Options:

 -   **Primary**: Attempted first to identify the caller.
-   **Fallback**: Attempted if the primary identifier does not return a match.


</td></tr><tr><td>

Active

</td><td>

Option to set the configuration active.

</td></tr></tbody>
</table>    \[Omitted image "configure-kba-question-answer-service.png"\] Alt text: Knowledge Based Question Service Mapping

4.  Select **Submit**.


## Result

You're redirected to the Knowledge Based Question Service Mappings list view. Verify if your mapping is successfully added.

\[Omitted image "configure-kba-question-answer-service-result.png"\] Alt text: Knowledge Based Question Service Mapping - Result

