---
title: Reviewing calculation details with formula trees
description: Review calculated metric definitions by viewing a structured and visual representation of the entire calculation chain. By using a formula tree, you can access the calculation details and view how the different metrics and emission factors are interconnected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/operational-sustainability-management/reviewing-formula-tree.html
release: australia
product: Operational Sustainability Management
classification: operational-sustainability-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using GRC: Metrics to provide data, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Reviewing calculation details with formula trees

Review calculated metric definitions by viewing a structured and visual representation of the entire calculation chain. By using a formula tree, you can access the calculation details and view how the different metrics and emission factors are interconnected.

The formula tree is a tool that enhances transparency in calculated metric values. Navigate to the calculated metric data record you want and view the formula tree, which shows a detailed breakdown of the calculation. It displays the values of the operands and how they’re combined to produce the final result. This feature helps users and auditors understand and verify the accuracy of complex calculations.

**Note:** Formula trees are available for the generated Calculated metric data when the **Calculation level** is set to Metric Definition and for the generated metrics when the **Calculation level** is set to Entity. For more information on Formula building, see [Formula building in a calculated metric definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/formula-building-at-metric-definition-and-entity-level.md).

As shown in the following examples, you can navigate to the calculated metric data record and select **Show formula tree** to view the associated formula tree.

\[Omitted image "metric-formula-tree.png"\] Alt text: Accessing the formula tree. For the text description, refer to the text that preceded this example.

\[Omitted image "metric-formula-tree-view.png"\] Alt text: Viewing the formula tree. For the text description, refer to the text that preceded this example.

**Note:** A formula tree displays the values of operands by applying the level of precision provided in the CMD.

For example, if the CMD specifies a precision of 2 decimal places, the formula tree displays all operand values with two decimal places, even if the actual values have more or fewer decimal places.

As shown in the following examples, if you’re seeing an empty page, it's because the formula tree or formula operands are currently empty and are being updated asynchronously. If you’re seeing an error page, it's due to errors in the formula operands that must be corrected.

**Note:** If a value is missing for any operand in a CMD formula, you can use the Calculated Metric Definition Settings table to define a default value for that operand. The system will automatically retrieve and apply the specified default value, ensuring the formula executes without interruption. Users can customize these default values or add new records as needed to suit their calculation requirements. For more information, refer to .

\[Omitted image "formula-tree-empty.png"\] Alt text: Viewing an empty page. For the text description, refer to the text that preceded this example.

\[Omitted image "formula-tree-error.png"\] Alt text: Viewing an empty page. For the text description, refer to the text that preceded this example.

To learn more about formula trees, see:

-   **[View the calculation breakdown in a formula tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/view-formula-tree.md)**  
View a structured and visual representation of the entire calculation chain.

**Parent Topic:**[Using GRC: Metrics to provide data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/using-grc-metrics.md)

