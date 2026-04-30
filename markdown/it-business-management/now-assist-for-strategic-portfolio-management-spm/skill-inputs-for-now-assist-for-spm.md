---
title: Skill inputs for Now Assist for Strategic Portfolio Management \(SPM\)
description: Learn about the inputs of each skill for the Now Assist for Strategic Portfolio Management \(SPM\) application. By configuring the inputs for a skill, you can determine how and when a skill is used.
locale: en-US
release: xanadu
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [Inputs for Now Assist for SPM, Inputs for the feedback summarization skill]
breadcrumb: [Configure, Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Skill inputs for Now Assist for Strategic Portfolio Management \(SPM\)

Learn about the inputs of each skill for the Now Assist for Strategic Portfolio Management \(SPM\) application. By configuring the inputs for a skill, you can determine how and when a skill is used.

## Now Assist for Strategic Portfolio Management \(SPM\) Overview

Depending on the selected skill, you can configure inputs. These settings determine how a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a feedback summary. If you have the admin role and any input fields are editable, you can modify the input data for a skill.

## Feedback summarization skill inputs

The feedback summarization skill includes the inputs that identify the table and fields that are used when a feedback summary is generated. The data source contains the tables and fields that the skill relies on. The following table lists the inputs for the feedback summarization skill.

<table id="table_tyn_brp_fbc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Feedback \[sn\_align\_core\_feedback\]

</td></tr><tr><td>

Fields

</td><td>

-   Name
-   Description

</td></tr></tbody>
</table>## Agile story generation skill inputs

The Agile story generation skill includes the inputs that identify the table and fields that are used to generate story recommendations for epics and features. The following table provides more details on the input data.

<table id="table_xvc_jgw_1fc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Epic \[sn\_align\_core\_scrum\_epic\]

</td></tr><tr><td>

Fields

</td><td>

-   Name
-   Description

</td></tr><tr><td>

Maximum stories to generate

</td><td>

This is the default number of stories that Now Assist recommends when a user prompts to create stories for an epic.If you have the admin role, you can modify this number. Choose from 3, 4, and 5.

</td></tr></tbody>
</table><table id="table_trw_ngw_1fc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Feature \[sn\_align\_core\_feature\]

</td></tr><tr><td>

Fields

</td><td>

-   Name
-   Description

</td></tr><tr><td>

Maximum stories to generate

</td><td>

This is the default number of stories that Now Assist recommends when a user prompts to create stories for a feature.If you have the admin role, you can modify this number. Choose from 3, 4, and 5.

</td></tr></tbody>
</table>## Write planning items skill inputs

<table id="table_ewq_22r_bfc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Planning item fields

</td><td>

Description

</td></tr><tr><td>

Story fields

</td><td>

-   Description
-   Acceptance criteria

</td></tr><tr><td>

Table

</td><td>

Product idea \[sn\_align\_core\_product\_idea\]

 Demand \[sn\_align\_core\_demand\]

 Capability \[sn\_align\_core\_capability\]

 Epic \[sn\_align\_core\_scrum\_epic\]

 Project \[sn\_align\_core\_project\]

 Feature \[sn\_align\_core\_feature\]

 Story \[rm\_story\]

</td></tr></tbody>
</table>**Related topics**  


[Configure Now Assist for Strategic Portfolio Management \(SPM\)](../task/configure-now-assist-for-spm.md)

[Exploring Now Assist for Strategic Portfolio Management \(SPM\)](../concept/exploring-now-assist-for-spm.md)

[Using AI agent agentic workflows in Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-na-spm-ai-agents.md)

[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

[Now Assist for SPM reference](now-assist-spm-reference.md)

