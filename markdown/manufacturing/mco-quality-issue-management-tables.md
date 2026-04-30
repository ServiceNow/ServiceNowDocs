---
title: Quality issue management tables
description: This section explains quality issue management \(QIM\) tables in Manufacturing Commercial Operations.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-01-05"
reading_time_minutes: 1
breadcrumb: [Quality issue management data model, Data model, Reference, Manufacturing Commercial Operations]
---

# Quality issue management tables

This section explains quality issue management \(QIM\) tables in Manufacturing Commercial Operations.

## QIM plugin

The QIM feature adds or modifies the existing tables:

-   Task \[sn\_customerservice\_task\]
-   RCA node category \[sn\_rca\_node\_category\]
-   Planning item \[sn\_align\_core\_planning\_item\]
-   Expense line \[fm\_expense\_line\]
-   Case
-   Complaint case \[sn\_complaint\_case\]

The QIM plugin adds the following tables.

<table id="table_mrd_cmf_whc"><thead><tr><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Stakeholder\[sn\_mfg\_qm\_stakeholder\]

</td><td>

Defines stakeholders for an issue with assigned RACI role and responsibility mapping.

</td></tr><tr><td>

Product Quality Investigation Task\[sn\_mfg\_qm\_prd\_qi\_task\]

</td><td>

Creates tasks for performing activities related to studying and gather further information on Quality Issue.

</td></tr><tr><td>

Product Quality Investigation\[sn\_mfg\_qm\_prd\_qi\]

</td><td>

Store the manufacturing quality issues that require deeper analysis.

</td></tr><tr><td>

Root Cause Analysis Task\[sn\_rm\_core\_rca\_task\]

</td><td>

Captures and manages the individual tasks created as part of a Root Cause Analysis \(RCA\) process.

</td></tr><tr><td>

Task Cause Association\[sn\_rm\_core\_task\_cause\_assoc\]

</td><td>

Associates tasks and RCA records with identified causes, including type classification.

</td></tr><tr><td>

Cause Category\[sn\_rm\_core\_cause\_category\]

</td><td>

Defines hierarchical categories for classifying issue causes.

</td></tr><tr><td>

Issue Cause\[sn\_rm\_core\_issue\_cause\]

</td><td>

Captures cause identified for an issue, with category and external reference.

</td></tr><tr><td>

Cause Action Plan\[sn\_rm\_core\_cause\_action\_plan\]

</td><td>

Links a cause to its defined action plan.

</td></tr><tr><td>

Cause Action\[sn\_rm\_core\_cause\_action\]

</td><td>

Associates a cause with the actions addressing it.

</td></tr><tr><td>

Remediation Action\[sn\_rm\_core\_rem\_action\]

</td><td>

Store the investigation related information.

</td></tr><tr><td>

Correction Action\[sn\_rm\_core\_correction\_action\]

</td><td>

Captures immediate actions taken to correct an identified issue.

</td></tr><tr><td>

Containment Action\[sn\_rm\_core\_containment\_action\]

</td><td>

Tracks short-term measures to contain or limit the impact of an issue.

</td></tr><tr><td>

Corrective Action\[sn\_rm\_core\_corrective\_action\]

</td><td>

Defines long-term actions implemented to eliminate the root cause of an issue.

</td></tr><tr><td>

Preventive Action\[sn\_rm\_core\_preventive\_action\]

</td><td>

Specifies proactive measures to avoid recurrence or future issues.

</td></tr><tr><td>

CoPQ Planned Line Charge\[sn\_rm\_core\_copq\_planned\_line\_charge\]

</td><td>

Defines planned cost line items for CoPQ financial requests, with unit cost, quantity, and type.

</td></tr><tr><td>

CoPQ Financial Request\[sn\_rm\_core\_copq\_fin\_req\]

</td><td>

Manages financial requests for CoPQ, including approvals.

</td></tr><tr><td>

CoPQ Expense Line\[sn\_rm\_core\_copq\_exp\_line\]

</td><td>

Captures actual cost entries linked to an action.

</td></tr><tr><td>

Product Non-conformance Case\[sn\_mfg\_qm\_prd\_ncc\]

</td><td>

Stores details of functional deviation/non-conformance of a product.

</td></tr><tr><td>

Product Non-conformance Case Task\[sn\_mfg\_qm\_prd\_ncc\_task\]

</td><td>

Creates task for performing activities related to studying and analyzing NC Case.

</td></tr><tr><td>

Impacted Asset\[sn\_mfg\_qm\_impacted\_asset\]

</td><td>

Tracks assets impacted by a reported issue, including their status and linkage to install base records.

</td></tr><tr><td>

Impacted Asset Action\[sn\_mfg\_qm\_impacted\_asset\_action\]

</td><td>

Links actions to impacted assets for issue resolution tracking.

</td></tr></tbody>
</table>**Parent Topic:**[Quality issue management data model](mco-quality-issue-management-data-model.md)

