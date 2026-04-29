---
title: Quick start tests for GRC Advanced Risk
description: Validate that Advanced Risk still works after you make any configuration change, such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Risk Management detailed setup, Configure, Risk Management, Governance, Risk, and Compliance]
---

# Quick start tests for GRC Advanced Risk

Validate that Advanced Risk still works after you make any configuration change, such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

## GRC Advanced Risk

GRC: Advanced Risk quick start tests require activating the GRC: Advanced Risk plugin \(com.sn\_risk\_advanced\) and loading the demo data.

<table id="table_hdb_wct_knb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

GRC: Create a Risk Event

</td><td>

Validates the creation of risk events.

</td><td>

New York

</td></tr><tr><td>

GRC: Create Risk Statement Hierarchy

</td><td>

Validates if the risk statement has a parent field so that the hierarchy can be maintained among risk statements

</td><td>

New York

</td></tr><tr><td>

GRC: Reject a Risk Event

</td><td>

Validates the rejection functionality the risk event

</td><td>

New York

</td></tr><tr><td>

GRC: Request more info - Risk Event

</td><td>

Validates the Request more information functionality before approving the risk event

</td><td>

New York

</td></tr><tr><td>

GRC: Create risk assessment scope

</td><td>

Creates different types of factors like manual factors, query factors, and automated scripted factor. It creates a Risk Assessment Methodology and associates the factors to the different assessment types in the Risk Assessment Methodology. It creates the Risk Assessment scope for the Risk Assessment Methodology. that has been set up.**Note:** While running ATF Tests, it is recommended to increase the test runner timeout from 120 seconds to approximately 240 seconds in the Test Runner Properties.

</td><td>

Orlando

</td></tr></tbody>
</table>To learn more about Advanced Risk, see [Download Advanced Risk](../../../product/grc-risk/task/download-risk-advanced.md)

**Parent Topic:**[Risk Management detailed setup](../../../product/grc-risk/concept/setup-risk-management.md)

