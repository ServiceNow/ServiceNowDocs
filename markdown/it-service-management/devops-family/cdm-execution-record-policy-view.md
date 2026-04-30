---
title: View the execution record for a policy run
description: View the execution record to analyze policy execution.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Validating and correcting configuration data, Use, DevOps Config, IT Service Management]
---

# View the execution record for a policy run

View the execution record to analyze policy execution.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_viewer or cdm\_editor or cdm\_exporter\_editor or cdm\_policy\_editor or cdm\_admin

## Procedure

1.  On the **Validation results** tab for a snapshot, select the more actions icon \(![More actions menu icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) for a policy and select **Execution record**.

<table id="table_dbd_mfl_gqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy

</td><td>

Name of the policy that executed.

</td></tr><tr><td>

Version name

</td><td>

Version of the policy that executed.

</td></tr><tr><td>

End time

</td><td>

Timestamp when execution finished.

</td></tr><tr><td>

Decision

</td><td>

Result of policy execution.

 -   Compliant
-   Non-compliant
-   Execution error
-   Compliant with exception


</td></tr></tbody>
</table>
