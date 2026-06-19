---
title: Knowledge-based authentication \(Security Questions\)
description: Knowledge-based authentication \(KBA\) is an identification and authentication method that verifies callers by prompting them to answer preconfigured questions across conversational AI channels, such as AI voice agents. KBA can be used to identify a caller, authenticate a caller, or both within the same interaction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/knowledge-based-authentication.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [KBA Security questions, Personal identification information, Authentication methods, Identity verification, Challenge questions, Secret answers, User authentication, Security Questions]
breadcrumb: [Configure authentication factors for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Knowledge-based authentication \(Security Questions\)

Knowledge-based authentication \(KBA\) is an identification and authentication method that verifies callers by prompting them to answer preconfigured questions across conversational AI channels, such as AI voice agents. KBA can be used to identify a caller, authenticate a caller, or both within the same interaction.

KBA validates answers against records in ServiceNow AI Platform tables. For callers whose data resides outside ServiceNow, admins can configure scripts to validate answers against external systems in real-time. External data is never imported or stored in ServiceNow AI Platform.

## How KBA works

**Identification** locates the caller by matching their answer to a record in ServiceNow AI Platform or an external system. For example, a caller provides their business phone number, and the system finds a matching record. Identification runs once per session and establishes who the caller is before any sensitive interaction begins.

**Authentication** verifies that the caller is who they claim to be. The caller answers one or more questions, and the system validates those answers against stored or externally sourced data.

KBA questions can be configured for identification, authentication, or both phases, depending on admin configuration.

## External source validation

When caller data is not stored in ServiceNow AI Platform, admins can configure a custom script on an answer record to validate the caller's response against an external system, such as a CRM or order management platform. The script receives the caller's answer as input and returns a match result.

-   For identification, the script returns the matched record.
-   For authentication, the script returns a `true` or `false` result.

**Note:** Only `snc_external` users can be authenticated using external source.

Script execution is limited to 15 seconds by default. To learn more configuration properties, see [System Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/create-knowledge-based-answers.md).

## Context persistence

Starting `"nowassist-aia-voice", version: "5.0.3"` release, answers collected during identification and authentication are persisted as session context and are available to subsequent authentication questions. This means a caller does not have to repeat information they already provided. For example, if a caller provides a booking reference during identification, that value is accessible to authentication scripts without prompting the caller again.

**Note:** Context persistence is available only for scripted answers, it doesn't capture non-scripted answer responses.

## Key strengths

-   No additional device or internet connectivity is required.
-   Familiar to most users.

## Limitations

-   KBA relies on information the caller knows, which can be guessed, obtained from public records, or exposed through social engineering.
-   KBA is not recommended as the sole verification method for sensitive operations.
-   KBA is best suited for low-risk scenarios, such as general IT support or public documentation access.

For detailed configuration instructions, see:

-   [Create KBA questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/create-knowledge-based-questions.md)
-   [Create KBA answers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/create-knowledge-based-answers.md)
-   [Map KBA questions to answers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/create-kba-answer-mappings.md)
-   [AI voice agent service mapping with KBA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/create-kba-service-mappings.md)

