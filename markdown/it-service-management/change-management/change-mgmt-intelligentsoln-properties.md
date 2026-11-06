---
title: Intelligent solutions system properties
description: Administrators can configure the Change Management Intelligent solutions system properties to use Predictive Intelligence capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/change-mgmt-intelligentsoln-properties.html
release: australia
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Predictive Intelligence for Change Management, Configure, Change Management, IT Service Management]
---

# Intelligent solutions system properties

Administrators can configure the Change Management Intelligent solutions system properties to use Predictive Intelligence capabilities.

By configuring these properties, you enable the Change Management application to:

-   Predict the risk of the proposed change.
-   Use similarity and clustering to identify and suggest potential standard change templates.

Navigate to **Change** &gt; **Intelligent Solution Configuration** to view and edit the properties.

## Risk Intelligence properties

The risk prediction surfaces on the change request based on the `chg_ml_prop_risk.usage` property. When set to **View risk value**, the prediction appears in an information message on the change request form. When set to **Set risk value**, the predicted value is written to the **Risk** field. For the conceptual overview, see [Predictive Intelligence for Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-mgmt-intelligent-solutions.md). For components installed with the plugin, see [Components installed with Change Management - Risk Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/installed-with-risk-intelligence.md).

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

Determines how the predictive value is used and where it appears on the change request.-   **View risk value**: Displays the prediction in an information message on the change request form without changing any field value.
-   **Set risk value**: Writes the predicted value to the **Risk** field on the change request.

</td></tr><tr><td>

Solution enabled \[chg\_ml\_prop\_risk.solution\_enabled\]

</td><td>

Identifies if the solution is enabled or not.

</td></tr><tr><td>

Threshold \[chg\_ml\_prop\_risk.classification\_confidence\_threshold\]

</td><td>

The minimum confidence value for the returned results.

</td></tr></tbody>
</table>## Standard change proposal properties

|Property|Description|
|--------|-----------|
|Minimum quality level \[chg\_ml\_prop\_sctp.quality\]|Minimum cluster quality to use for standard change candidates.|

**Parent Topic:**[Predictive Intelligence for Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-mgmt-intelligent-solutions.md)

