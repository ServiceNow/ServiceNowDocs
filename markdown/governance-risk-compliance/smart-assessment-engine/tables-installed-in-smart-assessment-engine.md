---
title: Tables installed in Smart Assessment Engine
description: Tables are added with activation of GRC: Smart Assessment Engine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/tables-installed-in-smart-assessment-engine.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: reference
last_updated: "2026-04-13"
reading_time_minutes: 8
breadcrumb: [Components installed with Smart Assessment Engine, Reference, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Tables installed in Smart Assessment Engine

Tables are added with activation of GRC: Smart Assessment Engine.

## Tables installed with Smart Assessment Core

<table id="table_ut1_5wq_t3c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment Template\[sn\_smart\_asmt\_template\]

</td><td>

Extends the sys\_metadata table and stores all assessment template definitions including name, description, publication status, versioning, and instructions.

</td></tr><tr><td>

Assessment Template Category\[sn\_smart\_asmt\_template\_category\]

</td><td>

Extends the sys\_metadata table and stores categories that classify assessment templates by purpose. Controls access via associated roles and defines assessment handling on version retirement.

</td></tr><tr><td>

Assessment Template Contributor\[sn\_smart\_asmt\_template\_contributor\]

</td><td>

Extends the sys\_metadata table. Many-to-many relationship table that is used to manage the relationships between assessment templates and user criteria for contributor access.

</td></tr><tr><td>

Section\[sn\_smart\_asmt\_section\]

</td><td>

Extends the sys\_metadata table and stores sections within assessment templates. Supports hierarchical structure with subsections via parent/child relationships.

</td></tr><tr><td>

Question\[sn\_smart\_asmt\_question\]

</td><td>

Extends the sys\_metadata table and stores question definitions within sections. Includes label, guidance, question type, data type, response layout, validation rules, and conditional configuration settings for visibility, justification, attachment, preferred answer, and response automation.

</td></tr><tr><td>

Question Type\[sn\_smart\_asmt\_question\_type\]

</td><td>

Extends the sys\_metadata table and stores the available question types such as Textbox, Dropdown, Radio, Checkbox, Number, Calendar, Attachment, Reference, and Barcode with their category, icons, and guidance.

</td></tr><tr><td>

Response Option\[sn\_smart\_asmt\_response\_option\]

</td><td>

Extends the sys\_metadata table and stores answer options for choice-based questions. Supports text, currency, number, and date response labels.

</td></tr><tr><td>

Assessment Condition\[sn\_smart\_asmt\_condition\]

</td><td>

Extends the sys\_metadata table and stores reusable condition definitions as encoded queries. Used for visibility, preferred answer, justification, and attachment conditions on questions.

</td></tr><tr><td>

Assessment Predicate\[sn\_smart\_asmt\_predicate\]

</td><td>

Extends the sys\_metadata table and stores predicate definitions linking conditions to assessment templates. Base table for specialized predicates such as response automation and scoring.

</td></tr><tr><td>

Response Automation Predicate\[sn\_smart\_asmt\_response\_automation\_predicate\]

</td><td>

Extends the Assessment Predicate \[sn\_smart\_asmt\_predicate\] table and stores automated response generation rules with support for scripted responses across various response types including text, number, date, and selected options.

</td></tr><tr><td>

Question to Assessment Condition\[sn\_smart\_asmt\_m2m\_question\_condition\]

</td><td>

Extends the sys\_metadata table. Many-to-many relationship table that is used to manage the mapping between questions and conditions, with condition types: visibility, preferred\_answer, attachment, and justification.

</td></tr><tr><td>

Assessment Persona\[sn\_smart\_asmt\_persona\]

</td><td>

Extends the sys\_metadata table and stores persona or role definitions for assessment participation such as assessor and reviewer.

</td></tr><tr><td>

Assessment Workflow State\[sn\_smart\_asmt\_workflow\_state\]

</td><td>

Extends the sys\_metadata table and stores workflow state definitions for assessment instances such as Draft, In Progress, and Completed.

</td></tr><tr><td>

Context Item\[sn\_smart\_asmt\_context\_item\]

</td><td>

Extends the sys\_metadata table and defines which external table records can be shown as context or references during assessment completion. Includes reference card field configuration.

</td></tr><tr><td>

Descriptive Image\[sn\_smart\_asmt\_descriptive\_image\]

</td><td>

Extends the sys\_metadata table and stores images associated with questions or sections to provide visual guidance, including alt text for accessibility.

</td></tr><tr><td>

Assessment Duration\[sn\_smart\_asmt\_duration\]

</td><td>

Stores time duration allocations for assessment templates.

</td></tr><tr><td>

Assessment Group\[sn\_smart\_asmt\_assessment\_group\]

</td><td>

Stores assessment group records that group multiple assessment instances together. Tracks group status as open or closed.

</td></tr><tr><td>

Smart Assessment Instance\[sn\_smart\_asmt\_instance\]

</td><td>

Stores individual assessment instances created from templates. Tracks assessment state, due dates, response completion metrics, and audit trail including requestor and assigned personas.

</td></tr><tr><td>

Assessment Section Instance\[sn\_smart\_asmt\_section\_instance\]

</td><td>

Stores runtime instances of sections for a specific assessment. Tracks section-level question counts, unanswered required questions, unanswered required justifications, unanswered required attachments, and user comments.

</td></tr><tr><td>

Assessment Question Instance\[sn\_smart\_asmt\_question\_instance\]

</td><td>

Stores runtime instances of questions for a specific assessment. Captures user responses for text, number, date, currency, reference, and selected options. Also stores condition evaluation results for visibility, preferred answer, justification, and attachment along with response metadata.

</td></tr><tr><td>

Response Option Instance\[sn\_smart\_asmt\_response\_option\_instance\]

</td><td>

Stores the selected or unselected state of each response option for a specific question instance in an assessment.

</td></tr><tr><td>

Assessment Predicate Instance\[sn\_smart\_asmt\_predicate\_instance\]

</td><td>

Stores runtime instances of predicate evaluations during assessment execution, including condition result sets and final evaluation outcomes.

</td></tr><tr><td>

Assessment Condition Result Set\[sn\_smart\_asmt\_condition\_result\_set\]

</td><td>

Stores the aggregated boolean result of evaluated conditions at runtime. Referenced by question instances for visibility, preferred answer, justification, and attachment condition outcomes.

</td></tr><tr><td>

Assessment Condition Result\[sn\_smart\_asmt\_condition\_result\]

</td><td>

Stores individual condition evaluation results within a condition result set, including the table, record, operator, and boolean outcome.

</td></tr><tr><td>

Assessment Scope Item\[sn\_smart\_asmt\_scope\_item\]

</td><td>

Stores records from other tables that are in scope for an assessment as table and record references.

</td></tr><tr><td>

Assessment Instance to Scope Item\[sn\_smart\_asmt\_m2m\_instance\_scope\_item\]

</td><td>

Many-to-many relationship table that is used to manage the mapping between assessment instances and scope items.

</td></tr><tr><td>

Assessment Instance to Persona to Users\[sn\_smart\_asmt\_m2m\_instance\_persona\]

</td><td>

Many-to-many relationship table that is used to map users to personas for specific assessment instances. Tracks persona-level ownership via primary owner.

</td></tr><tr><td>

Smart Assessment Combined Assessment\[sn\_smart\_asmt\_combined\_assessment\]

</td><td>

Stores combined assessment records that aggregate multiple assessment instances into a unified view with aggregated metrics and auto-copy capability.

</td></tr><tr><td>

Assessment Instance to Combined Assessment\[sn\_smart\_asmt\_m2m\_instance\_combined\_assessment\]

</td><td>

Many-to-many relationship table that is used to manage the mapping between assessment instances and combined assessments, with aggregated question counts.

</td></tr><tr><td>

Assessment Template Transaction\[sn\_smart\_asmt\_assessment\_template\_transaction\]

</td><td>

Stores template-level transaction records for operations such as publish, move to draft, copy, and create version. Tracks transaction status and error details.

</td></tr><tr><td>

Combined Assessment Transaction\[sn\_smart\_asmt\_combined\_assessment\_transaction\]

</td><td>

Stores transaction records for copying responses, justifications, and attachments between combined assessment instances. Tracks transaction type and status.

</td></tr></tbody>
</table>## Tables installed with Smart Assessment Scoring

<table id="table_nnj_cxq_t3c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric\[sn\_smart\_scoring\_metric\]

</td><td>

Extends the sys\_metadata table and stores scoring metric definitions for assessments, with support for normalization strategies.

</td></tr><tr><td>

Pre Defined Metric\[sn\_smart\_scoring\_pre\_defined\_metric\]

</td><td>

Extends the Metric \[sn\_smart\_scoring\_metric\] table and stores pre-built metrics based on questions, sections, or subsections with aggregation strategies including average, maximum, minimum, sum, and weighted average.

</td></tr><tr><td>

Metric Instance\[sn\_smart\_scoring\_metric\_instance\]

</td><td>

Stores runtime metric score values for a specific assessment instance, including both raw and normalized scores.

</td></tr><tr><td>

Metric Mapping\[sn\_smart\_scoring\_metric\_mapping\]

</td><td>

Extends the sys\_metadata table. Many-to-many relationship table that is used to map metrics to sections within assessment templates for score aggregation.

</td></tr><tr><td>

Question Scoring Predicate\[sn\_smart\_scoring\_question\_scoring\_predicate\]

</td><td>

Extends the Assessment Predicate \[sn\_smart\_asmt\_predicate\] table and stores question-specific scoring rules with aggregation strategies and optional normalization.

</td></tr><tr><td>

Scoring Normalization Strategy\[sn\_smart\_scoring\_normalization\_strategy\]

</td><td>

Extends the sys\_metadata table and stores reusable, system-provided normalization strategies defined via scripts. Read-only.

</td></tr><tr><td>

Scoring Normalization Strategy Input\[sn\_smart\_scoring\_normalization\_strategy\_input\]

</td><td>

Extends the sys\_metadata table and defines input parameters of number or choice type for normalization strategies. Read-only.

</td></tr><tr><td>

Scoring Normalization Strategy Input Choice\[sn\_smart\_scoring\_normalization\_strategy\_input\_choice\]

</td><td>

Extends the sys\_metadata table and stores choice values for choice-type normalization strategy inputs. Read-only.

</td></tr><tr><td>

Scoring Normalization Strategy Input Mapping\[sn\_smart\_scoring\_normalization\_strategy\_input\_mapping\]

</td><td>

Extends the sys\_metadata table and maps specific values to normalization strategy inputs at the template level for questions or metrics.

</td></tr></tbody>
</table>## Tables installed with Reusable Impact Framework

<table id="table_obg_2xq_t3c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automated Action\[sn\_impact\_fwk\_automated\_action\]

</td><td>

Extends the sys\_metadata table and stores automated action definitions that reference Flow Designer subflows with input configuration.

</td></tr><tr><td>

Automated Action Context\[sn\_impact\_fwk\_automated\_action\_context\]

</td><td>

Stores execution context for automated actions, including flow context, inputs, outputs, and execution status.

</td></tr></tbody>
</table>**Note:** All additional tables installed by the dependent plugins are also needed for Smart Assessment Engine. The Scoring plugin also adds scoring-related fields such as **enable\_scoring**, **weight**, **default\_score**, **score**, and **normalized\_score** to core tables such as sn\_smart\_asmt\_question, sn\_smart\_asmt\_template, sn\_smart\_asmt\_section, sn\_smart\_asmt\_question\_instance, and sn\_smart\_asmt\_section\_instance.

## Tables installed with Smart Assessment Collaboration

<table id="table_collab"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Section Instance to Persona to Users\[sn\_smart\_collab\_m2m\_section\_instance\_persona\]

</td><td>

Many-to-many relationship table that maps section instances to personas and their contributing users within an assessment instance.

</td></tr></tbody>
</table>## Tables installed with Smart Assessment Now Assist

<table id="table_now_assist"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Response\[sn\_smart\_ai\_assist\_ai\_response\]

</td><td>

Extends the Assessment Question Instance \[sn\_smart\_asmt\_question\_instance\] table and stores AI-generated response suggestions for assessment questions, including the generation trigger, target question instance, and acceptance state.

</td></tr><tr><td>

AI Response Source\[sn\_smart\_ai\_assist\_ai\_response\_source\]

</td><td>

Stores source references for AI-generated responses. Base table for specialized source types such as record sources.

</td></tr><tr><td>

AI Response Record Source\[sn\_smart\_ai\_assist\_ai\_response\_record\_source\]

</td><td>

Extends the AI Response Source \[sn\_smart\_ai\_assist\_ai\_response\_source\] table and stores specific record references used as sources for AI response generation, including table, record, and reason.

</td></tr><tr><td>

AI Response Transaction\[sn\_smart\_ai\_assist\_ai\_response\_transaction\]

</td><td>

Stores transaction records for AI response generation operations on assessment instances, tracking status, source types, question counts, and auto-populate settings.

</td></tr><tr><td>

AI Transaction Result\[sn\_smart\_ai\_assist\_ai\_transaction\_result\]

</td><td>

Stores individual results for each question within an AI response transaction, including source type, status, error details, and generated AI responses.

</td></tr></tbody>
</table>## Tables installed with Smart Assessment Impact Automation

<table id="table_impact_auto"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment Automation Rule\[sn\_smart\_imp\_auto\_rule\]

</td><td>

Extends the sys\_metadata table and stores automation rule definitions for assessment templates, including name, description, publication status, and enabled state.

</td></tr><tr><td>

Assessment Action Set\[sn\_smart\_imp\_auto\_action\_set\]

</td><td>

Extends the Assessment Predicate \[sn\_smart\_asmt\_predicate\] table and stores action set definitions that group assessment actions under an automation rule.

</td></tr><tr><td>

Assessment Action\[sn\_smart\_imp\_auto\_assessment\_action\]

</td><td>

Extends the Automated Action \[sn\_impact\_fwk\_automated\_action\] table and stores assessment-specific automated actions linked to action sets and assessment templates, with active state and base record tracking.

</td></tr><tr><td>

Assessment Action Set Instance\[sn\_smart\_imp\_auto\_action\_set\_instance\]

</td><td>

Extends the Assessment Predicate Instance \[sn\_smart\_asmt\_predicate\_instance\] table and stores runtime instances of action set evaluations during assessment execution.

</td></tr><tr><td>

Assessment Automated Action Context\[sn\_smart\_imp\_auto\_action\_context\]

</td><td>

Extends the Automated Action Context \[sn\_impact\_fwk\_automated\_action\_context\] table and stores execution context for assessment-specific automated actions, linking rule instances to assessment instances.

</td></tr><tr><td>

Assessment Rule Instance\[sn\_smart\_imp\_auto\_rule\_instance\]

</td><td>

Stores runtime instances of automation rules for specific assessment instances, linking automation rules to their execution context.

</td></tr><tr><td>

Template Category to Action Category\[sn\_smart\_imp\_auto\_m2m\_temp\_cat\_to\_action\_cat\]

</td><td>

Extends the sys\_metadata table. Many-to-many relationship table that maps assessment template categories to Flow Designer action categories.

</td></tr></tbody>
</table>## Tables installed with Smart Assessment Response Automation

<table id="table_resp_auto"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Response Automation Predicate Instance\[sn\_smart\_resp\_auto\_predicate\_instance\]

</td><td>

Extends the Assessment Predicate Instance \[sn\_smart\_asmt\_predicate\_instance\] table and stores runtime instances of response automation predicate evaluations, including question instance reference and error details.

</td></tr></tbody>
</table>## Tables installed with Smart Assessment Migration Tools

<table id="table_mig_tools"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment Template Migration\[sn\_smart\_asmt\_mig\_template\_migration\]

</td><td>

Stores migration records for converting legacy assessment metric types to smart assessment templates, tracking source, target, purpose, migration status, and errors.

</td></tr><tr><td>

Section Migration\[sn\_smart\_asmt\_mig\_section\_migration\]

</td><td>

Stores migration records for converting legacy metric categories to smart assessment sections within a template migration.

</td></tr><tr><td>

Question Migration\[sn\_smart\_asmt\_mig\_question\_migration\]

</td><td>

Stores migration records for converting legacy metrics to smart assessment questions within a section migration.

</td></tr><tr><td>

Response Option Migration\[sn\_smart\_asmt\_mig\_response\_option\_migration\]

</td><td>

Stores migration records for converting legacy metric definitions and template definitions to smart assessment response options within a question migration.

</td></tr></tbody>
</table>