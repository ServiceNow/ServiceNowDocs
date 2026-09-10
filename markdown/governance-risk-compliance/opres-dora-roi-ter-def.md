---
title: Define terminology for ROI export
description: Define your organization's terminology for closed-set indicator options in the Register of Information. This verifies the B\_99.01 export includes your definitions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/opres-dora-roi-ter-def.html
release: australia
topic_type: task
last_updated: "2026-08-11"
reading_time_minutes: 1
breadcrumb: [Exploring Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Define terminology for ROI export

Define your organization's terminology for closed-set indicator options in the Register of Information. This verifies the B\_99.01 export includes your definitions.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

Template B\_99.01 requires your organization to provide its own internal definition for every closed-set option used across the other Register of Information \(RoI\) templates. For example, if B\_07.01 rates the impact of discontinuing an ICT service as Low, Medium, or High, you must define what those terms mean within your organization.

The **Terminology Definitions** module provides a fixed list of the 19 closed-set options that require a definition, pre-populated by the system. You can't create or delete rows; you can only add or edit the internal definition for each option. If you leave a definition empty, the B\_99.01 export still succeeds, with an empty value for that option.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Terminology Definitions**.

2.  Review the list of 19 options.

    Each row shows the row code, CSV column, EBA column code, column name, and option label; these fields are read-only.

3.  Select the **Internal definition** field for an option and enter your organization's definition.

4.  Repeat for each option that applies to your organization's Register of Information submissions.

    Your definitions are saved and are included the next time you generate the B\_99.01 export.


**Parent Topic:**[Exploring Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/exploring-digi-resi-third-party-registers.md)

