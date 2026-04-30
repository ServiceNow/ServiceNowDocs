---
title: Inputs and triggers for Now Assist for Security Incident Response
description: You can configure some of the inputs or triggers for a generative AI skill. Inputs or triggers permit you to determine how and when a skill is used.
locale: en-US
release: yokohama
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: reference
last_updated: "2026-01-15"
reading_time_minutes: 2
keywords: [Now Assist Security Operations]
breadcrumb: [Configure, Now Assist for Security Incident Response, Security Operations]
---

# Inputs and triggers for Now Assist for Security Incident Response

You can configure some of the inputs or triggers for a generative AI skill. Inputs or triggers permit you to determine how and when a skill is used.

## Inputs and triggers

Inputs identify the data used for a skill. Inputs include the table and fields used to generate a security incident summary. A trigger initiates an action. For example, triggers determine when the system generates a summary.

You can modify inputs and triggers, but you can't modify a skill's data source. The data source contains the tables and fields that the skill relies on.

## Security incident summarization skill

Inputs for the security incident summarization skill identify the table and fields used when a security incident summary is generated. The following table lists the inputs for the Security Incident summarization skill from the Choose Input page in the Now Assist Admin console.

<table id="table_arz_fk3_1cc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

Security Incident \[sn\_si\_incident\] table.

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   State
-   Priority
-   Work notes
-   Additional comments

</td></tr><tr><td>

Related Input tables

</td><td>

-   Affected CIs - configuration item
-   Affected Users - Users
-   Security Incident Response Task - Short description
-   State - Any state other than **Cancelled**.
-   Associated Observables - Observable finding is Malicious or Suspicious.

</td></tr></tbody>
</table>## Resolution notes generation skill

Inputs for the Resolution notes generation skill identify the table and fields that are used when the resolution notes are generated for a security incident. The following table lists the inputs for the resolution notes generation skill from the Choose Input page in the Now Assist Admin console.

<table id="table_il3_sfj_1cc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

Security Incident \[sn\_si\_incident\] table.

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Work notes
-   Additional comments

</td></tr></tbody>
</table>## Security incident recommended actions generation skill

|Input|Description|
|-----|-----------|
|Data source|Security Incident \[sn\_si\_incident\] table.|

## Post incident analysis generation skill

|Input|Description|
|-----|-----------|
|Data source|Security Incident \[sn\_si\_incident\] table.|

## Correlation insights generation skill

Your correlation insights for a security incident can contain records from the following tables, but you must have permission to access these tables and records.

<table id="table_ytl_2l5_pdc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

Security Incident \[sn\_si\_incident\] table.

 Configuration item \[cmdb\_ci\] table.

 Incident \[incident\] table.

 Change request \[change\_request\] table.

 Problem \[problem\] table.

 Vulnerable item \[sn\_vul\_vulnerable\_item\] table.

 Associate observable \[sn\_ti\_observable\] table.

</td></tr></tbody>
</table>## Security Incident Quality Assessment

Your Quality Assessment report for a security incident can contain records from the following tables, but you must have permission to access these tables and records.

<table id="table_k2k_zc4_jhc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

Security Incident \[sn\_si\_incident\] table.

 Configuration item \[cmdb\_ci\] table.

 Task CI \[task\_ci\]

 Associated Observable \[sn\_ti\_observable\]

 Affected Users \[sn\_si\_m2m\_task\_affected\_user\]

 Security Incident Task \[sn\_si\_task\]

 Task SLA \[task\_sla\]

 Email \[sys\_email\]

 Playbook Activities: sys\_pd\_activity\_context

</td></tr></tbody>
</table>