---
title: Configure a business impact analysis template
description: Define the business impact analysis \(BIA\) template to create and assign BIAs with standard object types. The object types can be business processes, applications, facilities, and others, the impact of which are assessed in a BIA.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/configure-bia-template.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [BCM in the Classic Workspace, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure a business impact analysis template

Define the business impact analysis \(BIA\) template to create and assign BIAs with standard object types. The object types can be business processes, applications, facilities, and others, the impact of which are assessed in a BIA.

## Before you begin

Role required: sn\_bcm.admin

## About this task

By configuring a BIA template, you can:

-   Define the primary object type that the template is to be used for.
-   Choose the specific impact categories to be assessed during the BIA.
-   Define the types of dependencies that should be identified during the BIA.

During a business impact analysis of a primary element, you can also assess its recovery time based on data backup requirements. Technology assets related to a server or database store critical information and require data backup. Filter impact categories by Recovery Time Objective or Recovery Point Objective to identify the recovery objective of critical primary elements.

If the primary element requires data backup, set the **Requires data backup** field to **Yes** in the [Element Definition form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configure-element-definitions.md). All impact categories then appear in the **Impact Categories** field, whether they contribute to Recovery Point Objective or Recovery Time Objective. If the primary element does not require data backup, only impact categories that contribute to RTO are displayed.

## Procedure

1.  Navigate to **Business Continuity** &gt; **BIA Configuration** &gt; **BIA Templates**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_k3d_xgj_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the BIA template.

</td></tr><tr><td>

Description

</td><td>

Brief description about the template.

</td></tr><tr><td>

Primary Element Assessed

</td><td>

Primary object type or an element for which the template is used.

</td></tr><tr><td>

Impact Categories

</td><td>

Category of impact that an organization can confront. It can be revenue, legal, regulatory, reputation, and others.

</td></tr><tr><td>

Dependency Assessments

</td><td>

Category of items or assets that the business function depends on.

</td></tr><tr><td>

Include CIA

</td><td>

Option to include Confidentiality, Integrity, and Availability to BIA.The field appears only if the **Primary Element Assessed** field requires data backup. If the primary element requires data backup, set the flag as **Yes** in the Element Definitions form. See [Configure element definitions for Business Continuity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configure-element-definitions.md) Management.

</td></tr></tbody>
</table>4.  Click **Submit**.


