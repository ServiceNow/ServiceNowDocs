---
title: Intelligent solutions system properties
description: Administrators can configure the Change Management Intelligent solutions system properties to use predictive intelligence \(PI\) capabilities.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Predictive Intelligence for Change Management, Configure, Change Management, IT Service Management]
---

# Intelligent solutions system properties

Administrators can configure the Change Management Intelligent solutions system properties to use predictive intelligence \(PI\) capabilities.

By configuring these properties, you enable the Change Management application to:

-   Predict the risk of the proposed change.
-   Use similarity and clustering to identify and suggest potential standard change templates.

Navigate to **Change** &gt; **Intelligent Solution Configuration** to view and edit the properties.

## Risk Intelligence Properties

<table id="table_knq_tgs_mlb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Solution type \[chg\_ml\_prop\_risk.model\_type\]

</td><td>

The type of PI solutions used for risk prediction.-   Similarity: Uses machine-learning solution to collect and compare your existing records to new similar records. This solution type uses the following risk calculation method:

    -   Use count of records: Risk of the group that has highest count is used.​
    -   Use confidence of records: Risk of the group that has highest total number of confidence is used.​
If the risk have same count or confidence, then the higher risk is considered.

-   Classification: Uses machine-learning algorithms to set field values during record creation, such as setting the risk category based on previous data.

</td></tr><tr><td>

Predicted value usage \[chg\_ml\_prop\_risk.usage\]

</td><td>

Determines how the predictive value must be used.-   View risk value
-   Set risk value

</td></tr><tr><td>

Solution enabled \[chg\_ml\_prop\_risk.solution\_enabled\]

</td><td>

Identifies if the solution is enabled or not.

</td></tr><tr><td>

Threshold \[chg\_ml\_prop\_risk.classification\_confidence\_threshold\]

</td><td>

The minimum confidence value for the returned results.

</td></tr></tbody>
</table>## Standard Change Proposal Properties

|Property|Description|
|--------|-----------|
|Minimum quality level \[chg\_ml\_prop\_sctp.quality\]|Minimum cluster quality to use for Standard Change candidate.|

**Parent Topic:**[Predictive Intelligence for Change Management](../concept/change-mgmt-intelligent-solutions.md)

