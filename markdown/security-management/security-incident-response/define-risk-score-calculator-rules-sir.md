---
title: Define the new Risk Score Calculator Rules
description: Use the new Risk Score Calculator to define and calculate the risk score of security incidents based on the user-defined criteria, which provide a transparent intelligence scoring of security incidents. The risk score is auto-calculated for the security incident records.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configuring SIR Workspace, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Define the new Risk Score Calculator Rules

Use the new Risk Score Calculator to define and calculate the risk score of security incidents based on the user-defined criteria, which provide a transparent intelligence scoring of security incidents. The risk score is auto-calculated for the security incident records.

## Before you begin

Role required: sn\_si.admin.

Activate the new Risk Score Calculator by setting the `sn_si_aw.activate_new_risk_score_calculator` system property to true.

## About this task

Define a risk score for the security incident records that are generated based on the user-defined parameters. The base system is provisioned with one risk scoring rule, which can be customized and enabled accordingly.

**Note:**

-   By default, the new Risk Score Calculator Rule is inactive, and you need to enable the rule to see the risk score of the security incidents.
-   To calculate the risk score for additional related tables other than those available in the base system, refer to [Risk Score Calculator for Additional Related Tables](risk-score-calculator-related-tables.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace** &gt; **Administration**.

2.  Navigate to **Rules Engine** &gt; **Risk Score Calculator Rule**.

    The Risk Score Calculator Rule page is displayed.

    **Note:**

    -   As a part of the base system, you’re provided with one predefined risk scoring rule template to view, edit, or modify the risk score. However, you can’t create or delete the predefined risk score rule template.
    -   The changes you make will apply to any new security incidents or updates to the existing ones. To restate historical scores, use the **Recalculate Score** action.
3.  Select the **Risk Score Calculator** rule.

4.  On the form, fill the fields.

<table id="table_mhk_bd3_pyc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the risk score value. For example, Risk Score Calculator.

</td></tr><tr><td>

Overall weightage \(Applicable to criteria builder\)

</td><td>

Weightage of this field within the risk rule. This field isn’t editable and displays the overall weightage calculated by the system based on the weight corresponding to enabled criteria. The overall weightage should always be 100%.

</td></tr><tr><td>

Description

</td><td>

Description of the risk score record. For example, calculates risk score based on weighted sum of predefined criteria scores.

</td></tr><tr><td>

Scoring Criteria

</td><td>

Indicates the scoring criteria for a security incident.You can define the Risk **Scoring Criteria** using the following options:

-   **Criteria Builder**:

Use this option to add, edit, or remove, and enable and disable criteria that contribute to risk score calculation and verify that the total aggregated weightage is 100%.

-   **Use Script \(Advanced\)**: The scripting feature is an advanced feature to build a custom script that should return the risk score, which is an integer value ranging from 0 to 100.


</td></tr></tbody>
</table>5.  To define the **Scoring Criteria** using the **Criteria Builder**, perform the following steps:

    **Note:** You can edit or modify the existing criteria or add a new criteria.

    1.  To add a new criteria, select the **+New criteria** action.

        To ingest and map third-party risk scores, and factor them into security incident risk calculation or prioritization logic, use the **External risk score criteria** fields. To include NIST complaint incident prioritization, use the **Functional Impact**, **Information Impact**, **Recoverability** fields

    2.  Select the **Table** for which you want to set the criteria.

        **Note:**

        -   If the selected table is a security incident, the condition is applied to the security incident record for which the risk score is calculated. If the selected table isn’t a security incident, the condition is applied only if the records are related to the security incident for which the risk score is calculated.
        -   An additional Aggregate type is added to define the scores based on the number of relations associated with the security incidents.
    3.  Select the **Type** criteria for the selected table.

        The Type value could either be **Field** or **Aggregate** based on the table you choose.

    4.  Select the **Field** criteria for the selected table.

        If you selected the Type value as **Field**, then the Field criteria display the field values related to the table. If you selected the Type value as **Aggregate**, then the Field criteria display the aggregate values related to the table.

        **Note:** The Aggregate type supports only Count value.

        For example, if you select the Table criteria as **Security Incident**, then the Type criteria displays only **Field** option. The Field criteria display all the Field values related to the table, which could be Severity, Active, and so on Similarly, if you select the Table criteria as **Affected Users**, then the Type criteria displays both **Field** and **Aggregate** option. If you select the Type as Aggregate, the Field criteria display the aggregate values related to the table, which is **Count**.

    5.  Enter the **Weightage** of the criteria between 0-100.

        The overall weightage of all the criteria should be 100%.

    6.  Enter the name and a short description of the criteria.

    7.  Select the **Enable scoring criteria** check box to enable the scoring criteria.

    8.  Define the **Conditions** and set the score for the conditions.

    9.  You can also add new conditions using the **New Condition** option, and delete existing conditions using the **Delete Criteria** icon.

    10. Select **Add** to add the configured criteria.

        ![Scoring Criteria using Criteria Builder](../image/risk-score-calc-criteria-sir.png "Scoring Criteria using Criteria Builder")

6.  Select the **Recalculate Score** option to recalculate the risk score.

    For example, if there are changes to the risk score rule. In that case, you must reapply the scoring rule to the security incidents with the risk score already calculated in the past. Use the **Recalculate Score** action to trigger the recalculation job.

7.  Select **Confirm**.

    **Note:** Once your trigger this action, the process runs in the background and will take a few minutes to complete. You won't be able to make changes until it's finished.

8.  To define the **Scoring Criteria** using **Use Script \(Advanced\)** option, perform the following steps:

    1.  Use this predefined script to build a custom script that should return the risk score, which is an integer value ranging from 0 to 100.

        The advanced script field is auto-populated with a function, which takes the parameters **current** and this function should return the risk score, which is an integer value ranging from 0 to 100.

        ![Script Advanced option sample code](../image/risk-score-calc-sir.png "Scoring Criteria using Script (Advanced) option")

        Here, the current parameter is the GlideRecord object of the entity \(security incident\) for which the risk score is being calculated. For the security incidents, it corresponds to the GlideRecord for the sn\_si\_incident table.

9.  To disable the Risk Score Calculator, select **Disable**.

10. Select **Save**.


-   **[Risk Score Calculator for Additional Related Tables](risk-score-calculator-related-tables.md)**  
The Risk Score Calculator is provisioned with one risk-scoring rule as part of the base system to calculate the risk score of security incidents based on user-defined criteria. However, you can customize and include additional related tables to calculate the risk score.

**Parent Topic:**[Configuring SIR Workspace](../reference/configuring-security-incident-response-workspace.md)

**Related topics**  


[Set up view of SIR Records](../concept/set-up-view-of-sir-records.md)

[Configure SI design time investigation](../concept/configure-investigation-canvas-records.md)

[SIR Workspace Related Records](../concept/sir-records.md#)

[Configure Shift Handover](../concept/config-shift-handover.md)

[Security Incident Response conference call integration](../concept/sir-conf-call-capability.md)

[Configure report templates in Security Incident Response](../concept/daily-status-sir.md)

[On-Call scheduling in Security Incident Response](../concept/on-call-schedule-sir.md)

[Category management in Security Incident Response](../concept/category-management-sir.md)

