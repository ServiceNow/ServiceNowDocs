---
title: Skill inputs for Now Assist for Strategic Portfolio Management \(SPM\)
description: Learn about the inputs of each skill for the Now Assist for Strategic Portfolio Management \(SPM\) application. By configuring the inputs for a skill, you can determine how and when a skill is used.
locale: en-US
release: yokohama
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
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
</table>## Acceptance criteria generation skill inputs

The Acceptance criteria generation skill includes the inputs that identify the fields that are used as context to generate acceptance criteria for a story. The following table provides more details on the input data.

These inputs are available to configure for both Enterprise Agile Planning and Agile Development 2.0 applications.

<table id="table_bg2_3px_mhc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Story \[rm\_story\]This value can't be changed.

</td></tr><tr><td>

Fields

</td><td>

Short description, DescriptionYou can choose to add more fields to serve as context to generate acceptance criteria.

</td></tr><tr><td>

Acceptance criteria template

</td><td>

A default template is provided. You can choose to modify the existing template or define a new template based on your team's requirements.

</td></tr><tr><td>

Reference stories

</td><td>

Tag a story as a reference when it contains ideal acceptance criteria. These tagged stories serve as examples for Now Assist, giving it additional context to generate well-structured acceptance criteria for new stories.

</td></tr></tbody>
</table>## Refine records skill inputs

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

[Using AI agent or agentic workflows in Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-na-spm-ai-agents.md)

[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

[Now Assist for SPM reference](now-assist-spm-reference.md)

