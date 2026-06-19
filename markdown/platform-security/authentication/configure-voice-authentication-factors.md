---
title: Configure voice input for authentication factors
description: Configure how callers provide authentication responses by speaking or using the phone keypad.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/configure-voice-authentication-factors.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 1
breadcrumb: [Configure authentication factors for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Configure voice input for authentication factors

Configure how callers provide authentication responses by speaking or using the phone keypad.

## Before you begin

Role required: auth\_factors\_admin

**Note:**

-   For KBA, voice input is configured per question. For more information, see [Create KBA questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/create-knowledge-based-questions.md)
-   For all other numeric factors — Authenticator App \(TOTP\), Email OTP, SMS OTP, and Soft PIN, use the following procedure.

## Procedure

1.  Navigate to **All** &gt; **Authentication Factors** &gt; **Services** &gt; **Service Configurations**.

2.  Select **New**.

3.  Specify the following fields on the form.

<table id="table_wdd_l4j_kjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authentication Factor

</td><td>

Select the factor to configure. Options: **Authenticator App \(TOTP\)**, **Email OTP**, **SMS OTP**, **Soft PIN**.

</td></tr><tr><td>

Application

</td><td>

Global application scope is selected by default.

</td></tr><tr><td>

Service Profile Table

</td><td>

Select the table for the AI voice agent service.

 Leave empty to apply the configuration to all AI voice agent services.

</td></tr><tr><td>

Service Profile

</td><td>

Select the specific AI voice agent service the configuration applies to.

 Leave empty to apply the configuration to all AI voice agent services.

</td></tr><tr><td>

Input Type

</td><td>

Select how callers provide their response. Options:

 -   **Text**: The caller enters the response using the phone keypad.
-   **Voice**: The caller speaks the response aloud.
 When **Voice** is selected, the **Input Format Description**, **Input Format Example**, and **Input Validation Pattern** fields are displayed with preset values. These fields are read-only.

</td></tr><tr><td>

Input Format Description

</td><td>

This field appears only when **Input Type** is set to **Voice**. Expected format of the spoken response.

 Read-only. Preset by the platform for each factor.

</td></tr><tr><td>

Input Format Example

</td><td>

This field appears only when **Input Type** is set to **Voice**. Example spoken responses to guide the voice agent.

 Read-only. Preset by the platform for each factor.

</td></tr><tr><td>

Input Validation Pattern

</td><td>

This field appears only when **Input Type** is set to **Voice**. Regular expression pattern used to validate the transcribed response.

 Read-only. Preset by the platform for each factor.

</td></tr></tbody>
</table>    \[Omitted image "kba-service-config-1.png"\] Alt text: Service Configuration form with Input Type set to Voice

4.  Select **Submit**.


## Result

The input type configuration is saved. During an AI voice agent session, callers authenticate using the configured input method for the selected factor and service.

\[Omitted image "kba-service-config-2.png"\] Alt text: List of saved service configurations with input type and factor details

