---
title: Define terminology for the Register of Information export
description: Define your organization's internal definitions for the closed-set indicator options used across the Register of Information, so the B\_99.01 export includes your terminology rather than empty values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-dora-roi-terminology-definitions.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [DORA, Register of Information, B\_99.01, terminology definitions, TPRM]
breadcrumb: [Register of information regulatory packages, Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Define terminology for the Register of Information export

Define your organization's internal definitions for the closed-set indicator options used across the Register of Information, so the B\_99.01 export includes your terminology rather than empty values.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

Template B\_99.01 requires your organization to provide its own internal definition for every closed-set option used across the other Register of Information \(RoI\) templates. For example, if B\_07.01 rates the impact of discontinuing an ICT service as Low, Medium, or High, use B\_99.01 to define what each value means within your organization.

Rows can't be created or deleted; the only available action is to add or edit the internal definition for each option in the **Description** field. If you leave a description blank, the B\_99.01 export includes an empty value for that option.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Digital resilience third-party registers**.

2.  Select **Terminology and definitions**.

    Each row shows the **Row ID**, **Column Code**, **Column Name**, **Option**, and **Order**. These fields are read-only. The **Column Code** identifies the Register of Information field that the option applies to, using the EBA template and field numbering \(for example, `B_02.01.0020` refers to field 0020 on template B\_02.01\). Use it to identify which options are relevant to the RoI templates your organization submits. For descriptions of all fields, and the full mapping of all rows, see [Terminology and definitions fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-dora-roi-terminology-definitions-reference.md).

3.  Review the list of options to identify which require a definition for your organization.

4.  Enter a definition for an option.

    1.  Select the **Row ID** of the option to define.

    2.  Enter your organization's definition in the **Description** field.

5.  Save the record.

    Your definitions are saved and are included in the export the next time you generate the B\_99.01 export.

6.  Repeat for each option that applies to your organization's Register of Information submissions.


## What to do next

Your internal definitions are retained across upgrades and aren't overwritten. For more information about generating RoI packages, including the B\_99.01 export, see [Generate a register of information package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-roi-packages.md).

**Related topics**  


[Register of information regulatory packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-dora-roi.md)

[Generate a register of information package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-roi-packages.md)

