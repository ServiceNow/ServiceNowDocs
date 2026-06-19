---
title: Configure disambiguation
description: Configure the disambiguation property that controls when the assistant asks clarifying questions before responding to a Now Assist in Virtual Agent or Now Assist panel user request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/nava-configure-disambiguation-manually.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-03-30"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist Admin features, Now Assist, Enable AI experiences]
---

# Configure disambiguation

Configure the disambiguation property that controls when the assistant asks clarifying questions before responding to a Now Assist in Virtual Agent or Now Assist panel user request.

## Before you begin

Role required: admin

## About this task

Disambiguation or clarification helps the Now Assist assistant handle situations where the user's request is ambiguous. Rather than returning an overwhelming list of results, the assistant evaluates the request using a confidence scoring system and asks clarifying questions if needed.

## Procedure

1.  In the filter navigator field, enter `sys_properties.list`.

2.  In the selection fields, select **Name** from the drop-down list and enter `type_2_disamb` in the Search field.

3.  Configure the disambiguation property:

    If you have

    -   Now Assist in Virtual Agent or
    -   Now Assist panel \(standard chat, enhanced chat, or premium chat\)
    then use this configuration:

<table id="table_pkn_sn1_53c"><thead><tr><th>

Property

</th><th>

Possible values

</th><th>

Default value

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

sn\_aia.type\_2\_disamb

</td><td>

off/low/high

</td><td>

off

</td><td>

-   off - clarification is disabled. The assistant responds directly to all queries without asking follow-up questions.
-   low - clarification is triggered for highly ambiguous queries.
-   high - clarification is triggered more frequently, covering a broader range of ambiguous queries.


</td></tr></tbody>
</table>4.  To view the disambiguation data, in the filter navigator field, enter `sys_generative_ai_log`.


**Parent Topic:**[Configuring Now Assist Admin features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configuring-na-landing.md)

