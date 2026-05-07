---
title: Questionnaire Configuration form fields
description: You can define distinct questionnaire for a distinct collection of vulnerabilities or remediation tasks by filtering the vulnerabilities or remediation tasks respectively.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Questionnaire support in Exception Management via Smart Assessment, Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Questionnaire Configuration form fields

You can define distinct questionnaire for a distinct collection of vulnerabilities or remediation tasks by filtering the vulnerabilities or remediation tasks respectively.

The Questionnaire Configuration form appears when you select the **Design New Questionnaire** button in the configuration for Exception Management form for any one of the four applications.

<table id="table_tbz_5ws_gzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the questionnaire.

</td></tr><tr><td>

Approval rule

</td><td>

Approval rule for which the questionnaire is applicable.-   **Exception request for vulnerability groups**
-   **Exception request for vulnerable items**
-   **False positive for vulnerability groups**
-   **False positive for vulnerable items**
-   **Questionnaire for compensating controls for vulnerable groups** for remediation task's risk reduction requests.
-   **Questionnaire for compensating controls for vulnerable items** for vulnerable item's risk reduction requests.

</td></tr><tr><td>

Description

</td><td>

Short description for the questionnaire configuration.

</td></tr><tr><td>

Order

</td><td>

Questionnaire with lowest order appears during the requests.

</td></tr><tr><td>

Active

</td><td>

Enabled by default, signifying that the questionnaire is in use.

</td></tr><tr><td>

Table

</td><td>

Table for which the approval rule is applicable.-   Finding \[sn\_vul\_vulnerable\_item for the approval rules related to vulnerable items.
-   Remediation Task \[sn\_vul\_vulnerability\] for the approval rules related to remediation tasks.

</td></tr><tr><td>

Condition

</td><td>

Condition for the records for which the questionnaire must appear.You can apply condition on all the fields of a vulnerable item and remediation task except **Reason**.

</td></tr><tr><td>

Questionnaire

</td><td>

Questionnaire that appears when a remediation owner is requesting an exception, false positive or risk reduction.

</td></tr></tbody>
</table>**Parent Topic:**[Questionnaire support in Exception Management via Smart Assessment](../concept/sem-smart-assessment-exp-management.md)

