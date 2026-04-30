---
title: Knowledge-based authentication \(Security Questions\)
description: Knowledge-based authentication \(KBA\) is an identification and authentication method that verifies callers by prompting them to answer preconfigured questions across conversational AI channels, such as AI voice agents. KBA also supports validation against external systems through custom scripts, enabling identification of callers whose data resides outside ServiceNow AI Platform.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-11-12"
reading_time_minutes: 1
keywords: [KBA Security questions, Personal identification information, Authentication methods, Identity verification, Challenge questions, Secret answers, User authentication, Security Questions]
breadcrumb: [Configure authentication factors, Authentication factors, Authentication, Access Management]
---

# Knowledge-based authentication \(Security Questions\)

Knowledge-based authentication \(KBA\) is an identification and authentication method that verifies callers by prompting them to answer preconfigured questions across conversational AI channels, such as AI voice agents. KBA also supports validation against external systems through custom scripts, enabling identification of callers whose data resides outside ServiceNow AI Platform.

These questions leverage personal information that only the authorized user should know, such as the last four digits of their SSN. KBA relies on information known only to the caller, adding an extra layer of security for applications and services. However, due to the nature of this information, KBA is best suited for low-risk scenarios.

## Use Case

Low-risk authentication \(for example, general IT support, public documentation access, and so on\).

## Key Strengths

The KBA method offers the following advantages:

-   No additional device or internet connectivity required
-   Familiar to most users

## Important Considerations

While the KBA method is a convenient authentication method, there are several considerations to keep in mind:

-   Low security as answers can be guessed, obtained from public records, or exposed via social engineering.
-   Not recommended as the sole verification method for sensitive operations.

KBA can enhance overall security when used appropriately. For detailed configuration instructions, see:

-   [Create KBA questions](../task/create-knowledge-based-questions.md)
-   [Create KBA answers](../task/create-knowledge-based-answers.md)
-   [Map KBA questions to answers](../task/create-kba-answer-mappings.md)
-   [Assign KBA questions to your AI voice agent service](../task/create-kba-service-mappings.md)

