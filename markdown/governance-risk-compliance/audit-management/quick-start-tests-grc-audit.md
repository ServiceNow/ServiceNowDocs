---
title: Quick start tests for Audit Management
description: Validate that GRC: Audit Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Audit Management, Audit Management, Governance, Risk, and Compliance]
---

# Quick start tests for Audit Management

Validate that GRC: Audit Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

## GRC Audit Management

GRC: Audit Management quick start tests require activating the GRC: Audit Management plugin \(com.sn\_audit\) and loading the demo data.

<table id="atf-tests-audit-management"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

GRC: Create Audit Engagement and Generate Audit Task

</td><td>

Validates audit engagement creation and associates entities to generate controls and test plans. Generates audit task which is associated to a test plan.

</td><td>

Paris

</td></tr><tr><td>

GRC: Create and process a milestone

</td><td>

Create a milestone in an engagement, notice that the due date cannot be in past and the completion date cannot be in future and for a milestone in open state the percent complete is 0 which changes in accordance with the milestone state change.

</td><td>

Paris

</td></tr><tr><td>

GRC: Cost and Resource plan rollup

</td><td>

Create an audit plan and associate an engagement to it, on adding cost plan and resource plan to this engagement, notice that these costs are rolled up to the plan. Any edits to these costs in engagement reflects in the plan.

</td><td>

Paris

</td></tr><tr><td>

GRC: Create Engagement Project Manual and automatic

</td><td>

On an engagement in the validate state, once the Enable advanced planning ui-action is performed notice an engagement project gets created and when the state of an engagement associated to an audit plan having "Advanced planning capabilities" is changed to validate notice that an engagement project gets created automatically.

</td><td>

Paris

</td></tr><tr><td>

GRC: Auditable Unit with Detailed Risk Assessment

</td><td>

Create an Auditable unit with method as "Detailed Risk Assessment" and request for Assessing the Risk Assessment by adding the Assessor once the assessor responds and Marks Assessment as Complete after performing the control assessment and residual assessment, the risk assessment fields should be auto updated.

</td><td>

Paris

</td></tr></tbody>
</table>To learn more about Audit Management, see [Audit Management](../../../product/grc-audit/concept/c_GRCAudits.md).

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=australia&pubname=australia-application-development&ft:locale=en-US)

