---
title: Skill inputs for onboarding and engagement skills
description: Table and field inputs for the account onboarding case, engagement, success initiative, and executive insight skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-otto-skill-inputs-engagement.html
release: brazil
topic_type: reference
last_updated: "2026-09-22"
reading_time_minutes: 1
keywords: [skill inputs, engagement, onboarding]
breadcrumb: [Skill inputs, Reference, Customer Success Management]
---

# Skill inputs for onboarding and engagement skills

Table and field inputs for the account onboarding case, engagement, success initiative, and executive insight skills.

## Account onboarding case summarization skill

Includes the inputs that identify the table and fields used when an account onboarding summary is generated. You can configure the input in the following account onboarding case stages: Form details, Data capture, Development, Training, Testing.

<table id="table_inputs_onboarding_1"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Account Onboarding Case \[sn\_acct\_lc\_onb\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Service Exchange integration
-   Short description
-   Description
-   Go live date
-   Days remaining
-   Work notes
-   Additional comments

</td></tr></tbody>
</table><table id="table_inputs_onboarding_2"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Account Lifecycle Import Task

</td></tr><tr><td>

Input fields

</td><td>

-   State
-   Days remaining
-   Published records
-   Work notes
-   Additional comments
-   Target table
-   Total records updated

</td></tr></tbody>
</table><table id="table_inputs_onboarding_3"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Account Lifecycle Task

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   State
-   Days remaining
-   Type
-   Work notes
-   Additional comments

</td></tr></tbody>
</table>## Engagement summarization skill

Includes the inputs that identify the table and fields used when an engagement summary is generated.

<table id="table_inputs_engagement_1"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Engagement \[sn\_acct\_lc\_engagement\]

</td></tr><tr><td>

Input fields

</td><td>

-   State
-   Stage
-   Renewal date
-   Initial go-live date
-   Perceived health

</td></tr></tbody>
</table>|Related table|Input fields|
|-------------|------------|
|Risk and issue|State, Due date, Probability|
|Internal play|Due date, Progress|
|Success case|Due date, Progress|
|Success initiative|Due date, Progress|
|Success outcome|Progress, Base value, Current value, Target value|

## Success initiative summarization skill

Includes the inputs that identify the table and fields used when a success initiative summary is generated.

<table id="table_inputs_success_init_1"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Success initiative

</td></tr><tr><td>

Input fields

</td><td>

-   Primary success outcome
-   Account
-   Sold product name
-   Sold product number
-   Squad
-   Short description
-   Description
-   State
-   Contact
-   Days remaining

</td></tr></tbody>
</table>|Input|Description|
|-----|-----------|
|Input table|Success task|
|Input fields|State, Short description, Description, Due date, Days remaining|

## Executive Insight Generator skill

|Input|Description|
|-----|-----------|
|Input table|Activity type table \(sn\_actsub\_activity\_type\)|
|Input fields|activities|

**Parent Topic:**[Skill inputs for ServiceNow Otto for Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-otto-skill-inputs-reference.md)

