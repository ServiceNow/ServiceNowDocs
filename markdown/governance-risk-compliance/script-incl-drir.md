---
title: Script includes installed with Digital resilience incident reporting
description: Several Script includes are added to your instance with Digital resilience incident reporting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/script-incl-drir.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Digital resilience incident reporting reference, Reference, Operational Resilience, Governance, Risk, and Compliance]
---

# Script includes installed with Digital resilience incident reporting

Several Script includes are added to your instance with Digital resilience incident reporting.

<table id="table_m44_d2k_12c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DriIncRptgUtils

</td><td>

Contains common functions that are used across various components of the DRI application, such as business rules \(BR\), Script Actions, UI actions, and more. One important function within this module is getIntermediateDUE, which is used to modify the creation of intermediate report schedules.

</td></tr><tr><td>

DriIncRptgAjax

</td><td>

Contains functions that are used on the client side. It is a client-callable Script Include designed to provide important data to the client side.

</td></tr><tr><td>

DRIGenerateReport

</td><td>

Contains client-callable Script include that is used to generate or export Microsoft Excel files for reports.

</td></tr><tr><td>

DriIncRptgConstants

</td><td>

Stores all constants for the DRI application.

 This includes the sys\_ids of the DRI Initial report, DRI Intermediate report, DRI Final report, and Regulatory reporting assessment of IT incidents templates. DRIIncRptgResponseAutomation uses these sys\_ids to auto-fill responses across those templates. If you copy one of these templates to create a custom template, add new constants here for the custom template so that auto-fill keeps working. For more information, see [Set up DRI Smart Assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/set-up-sae-templates.md).

</td></tr><tr><td>

DRIIncRptgResponseAutomation

</td><td>

Used for response automation, which automatically populates certain questions based on data from previous templates, incidents, or source records.

 The fetchDefaultResponse method and \_asmtTemplateMapping object in this Script Include map each report template to the constants defined in DriIncRptgConstants. This mapping carries answers forward from one report to the next. Update this mapping whenever a custom template is used in place of, or alongside, the shipped templates. Automate response \(auto-fill\) currently does not support Reference-type questions, so answers to those questions aren't carried forward and must be entered manually on each report.

</td></tr><tr><td>

DriUserFilteringExtensionPoint

</td><td>

Provides filtering capabilities for contributors and collaborators on Digital resilience incident reporting assessment instances, enabling reassignment workflows.

</td></tr></tbody>
</table>