---
title: Choose input data form
description: The Choose input data form for the Regulatory alert summarization skill defines how data is structured and transmitted to the LLM, helping ensure integrity and relevance. It uses rule-based input templates and related taxonomy tables to provide contextual information for Default and New states.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate regulatory alert summarization skill, Configure, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Choose input data form

The Choose input data form for the Regulatory alert summarization skill defines how data is structured and transmitted to the LLM, helping ensure integrity and relevance. It uses rule-based input templates and related taxonomy tables to provide contextual information for Default and New states.

|Field|Description|
|-----|-----------|
|Base input table|Table used to determine where to pull the data from. This will be applicable to all the templates.|

<table id="table_bg2_p3q_xgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Default stateBase input table fields: each skill relies on a base input table and input fields with descriptions to provide context for the LLM to generate a response.

</td></tr><tr><td>

Base input field

</td><td>

Title

</td></tr><tr><td>

Field description

</td><td>

Alert Title

</td></tr><tr><td>

Base input field

</td><td>

Description

</td></tr><tr><td>

Field description

</td><td>

Alert Description

</td></tr><tr><td>

Base input field

</td><td>

Summary

</td></tr><tr><td>

Field description

</td><td>

Alert Summary

</td></tr><tr><td>

Base input field

</td><td>

Source publication date

</td></tr><tr><td>

Field description

</td><td>

Source publication date

</td></tr><tr><td>

Base input field

</td><td>

Effective date

</td></tr><tr><td>

Field description

</td><td>

Effective date

</td></tr><tr><td>

Base input field

</td><td>

Compliance date

</td></tr><tr><td>

Field description

</td><td>

Compliance date

</td></tr><tr><td class="sub-head" colspan="2">

Add rule conditions to the input templateRule conditions determine when the input template is used. By default, record state determines which input template the LLM uses.

</td></tr><tr><td>

Rule condition

</td><td>

Condition: state!=0^EQThis condition is only applied when the input template is applied only when the record is not in the default New state.

</td></tr><tr><td class="sub-head" colspan="2">

Add additional input data sources\(Related tables, Activity streams, Relationships, etc.\)

You can add input data sources like related tables, activity streams and relationships to provide more context to the LLM. You can also add rule conditions to these additional data sources.

</td></tr><tr><td>

Source Category

</td><td>

Description Category

</td></tr></tbody>
</table><table id="table_us2_nmr_xgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

New stateBase input table fields: each skill relies on a base input table and input fields with descriptions to provide context for the LLM to generate a response.

</td></tr><tr><td>

Base input field

</td><td>

Title

</td></tr><tr><td>

Field description

</td><td>

Alert Title

</td></tr><tr><td>

Base input field

</td><td>

Description

</td></tr><tr><td>

Field description

</td><td>

Alert Description

</td></tr><tr><td>

Base input field

</td><td>

Summary

</td></tr><tr><td>

Field description

</td><td>

Alert Summary

</td></tr><tr><td>

Base input field

</td><td>

Source publication date

</td></tr><tr><td>

Field description

</td><td>

Source publication date

</td></tr><tr><td>

Base input field

</td><td>

Effective date

</td></tr><tr><td>

Field description

</td><td>

Effective date

</td></tr><tr><td>

Base input field

</td><td>

Compliance date

</td></tr><tr><td>

Field description

</td><td>

Compliance date

</td></tr><tr><td class="sub-head" colspan="2">

Add rule conditions to the input templateRule conditions determine when the input template is used. By default, record state determines which input template the LLM uses.

</td></tr><tr><td>

Rule condition

</td><td>

Condition: state!=0^EQThis condition is only applied to the input template when the record isn’t in the default New state.

</td></tr><tr><td class="sub-head" colspan="2">

Add additional input data sources\(Related tables, Activity streams, Relationships, etc.\)

You can add input data sources like related tables, activity streams, and relationships to provide more context to the LLM. You can also add rule conditions to these additional data sources.

</td></tr><tr><td>

Select related input table

</td><td>

Regulatory alert to taxonomy-&gt;Regulatory alert

</td></tr><tr><td>

Related Table Field

</td><td>

Taxonomy

</td></tr><tr><td>

Field description

</td><td>

taxonomy name

</td></tr><tr><td>

Related Table Field

</td><td>

Class

</td></tr><tr><td>

Field description

</td><td>

taxonomy category

</td></tr></tbody>
</table>