---
title: Configure Risk Intelligence
description: Configure the Risk Intelligence properties to control how the Predictive Intelligence solution predicts the risk of a change request and how the predicted risk is used.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/configure-risk-intelligence.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-10-15"
reading_time_minutes: 3
breadcrumb: [Predictive Intelligence for Change Management, Configure, Change Management, IT Service Management]
---

# Configure Risk Intelligence

Configure the Risk Intelligence properties to control how the Predictive Intelligence solution predicts the risk of a change request and how the predicted risk is used.

## Before you begin

-   The Change Management - Risk Intelligence plugin \(com.snc.change\_management.ml.risk\) must be active.
-   The solution definition for the solution type that you plan to use must have an active trained solution. For more information, see [Train the Risk Intelligence solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/train-risk-intelligence-solution.md).

Role required: admin or sn\_change\_admin

## About this task

Risk Intelligence predicts the risk of a change request only when the solution is enabled and the selected solution definition has an active trained solution.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Intelligent Solution Configuration** &gt; **Risk Intelligence**.

    The Risk Intelligence Properties form opens.

2.  Select the **Solution enabled** check box.

    This option is selected by default. When the option is cleared, Risk Intelligence doesn't predict the risk of change requests.

3.  In the **Solution type** field, select an option.

    |Solution type|Description|
    |-------------|-----------|
    |**Classification**|Predicts the risk value by using a classification solution. This option is the default.|
    |**Similarity**|Predicts the risk value by using the change requests that are most similar to the current change request.|

    The form displays the fields for the selected solution type.

4.  On the form, fill in the fields for the selected solution type.

<table id="table_ri_solution_fields"><thead><tr><th>

Field

</th><th>

Solution type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Threshold

</td><td>

Classification

</td><td>

Minimum confidence value that a prediction must meet for Risk Intelligence to return a risk value. Predictions below this value aren't used. This field is required. The default value is 50.

</td></tr><tr><td>

Maximum number of results

</td><td>

Similarity

</td><td>

Maximum number of similar records to use when predicting risk. The default value is 100.

</td></tr><tr><td>

Risk calculation method

</td><td>

Similarity

</td><td>

Method used to base the risk prediction on the similar records that are returned.-   **Use count of records**: Bases the prediction on the number of results returned. This option is the default.
-   **Use confidence of records**: Bases the prediction on the confidence of the results returned.


</td></tr></tbody>
</table>5.  In the **Predicted value usage** field, select an option.

    |Option|Description|
    |------|-----------|
    |**View risk value**|Displays the predicted risk value for reference only. The predicted value doesn't change the risk of the change request. This option is the default.|
    |**Set risk value**|Includes the predicted risk value when the risk of the change request is calculated. If the predicted value is the highest risk across the risk evaluation methods, it's applied to the change request.|

6.  Select **Update**.

7.  To show the Risk Intelligence result in the risk details of a change request, set the **change.risk.show\_risk\_intelligence** system property.

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  Search for and open the **change.risk.show\_risk\_intelligence** property.

    3.  In the **Value** field, select an option.

        -   **Always**: Always shows the Risk Intelligence result, even when the solution is turned off or can't predict a value. This option is the default.
        -   **Has risk value**: Shows the Risk Intelligence result only when the solution is enabled and a prediction was made.
        -   **Never**: Never shows the Risk Intelligence result.
    4.  Select **Update**.

    This property applies to the risk details in both the core UI and Service Operations Workspace.

8.  To move the configuration to another instance, select **Add to Update Set** under **Related Links**.

    The Risk Intelligence properties and the solution definitions for the selected solution type are added to the current update set.


**Parent Topic:**[Predictive Intelligence for Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-mgmt-intelligent-solutions.md)

