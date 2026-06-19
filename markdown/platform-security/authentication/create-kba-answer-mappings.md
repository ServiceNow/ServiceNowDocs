---
title: Map KBA questions to answers
description: Create knowledge-based questions and answer mapping to confirm the user's identity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/create-kba-answer-mappings.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure KBA, Knowledge-based authentication, Configure authentication factors for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Map KBA questions to answers

Create knowledge-based questions and answer mapping to confirm the user's identity.

## Before you begin

Role required: auth\_factors\_admin

## Procedure

1.  Navigate to **All** &gt; **Authentication Factors** &gt; **Knowledge Based Factor** &gt; **Question Answer Mappings**.

2.  Select **New** on the Knowledge Based Question Answer Mappings page.

3.  Specify the following fields on the form:

    |Field|Description|
    |-----|-----------|
    |Question|Select the question that you would like to map with the answer. Example: `What is your business phone number?`|
    |Application|Global application scope is selected by default.|
    |Answer|Select the answer for mapping to the question. Example: `Business Phone Number`.|

    \[Omitted image "configure-kba-question-answer.png"\] Alt text: Knowledge Based Question Answer Mapping

4.  Select **Submit**.


## Result

You’re redirected to the Knowledge Based Question Answer Mappings list view. Verify if your mapping is successfully added.

\[Omitted image "configure-kba-question-answer-result.png"\] Alt text: Knowledge Based Question Answer Mappings - list

