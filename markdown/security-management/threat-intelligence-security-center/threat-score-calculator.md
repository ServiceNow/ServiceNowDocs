---
title: Define Threat Score Calculator
description: Define threat score for the observable\(s\) records that are generated based on the user defined parameters. The base system is provisioned with one threat scoring rule, which can be customized and enabled accordingly.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Custom Threat Score Calculator in TISC, About Rules Engine in TISC, Administer, Threat Intelligence Security Center, Security Operations]
---

# Define Threat Score Calculator

Define threat score for the observable\(s\) records that are generated based on the user defined parameters. The base system is provisioned with one threat scoring rule, which can be customized and enabled accordingly.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Note:** By default, the threat scoring rule will be inactive, you need to enable the rule to see the observables scoring.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Go to **Threat Scoring Rule**.

    The Threat Score Calculator page is displayed.

    **Important:**

    -   In the application, within the base system, there is one scoring rule which is provisioned for the users to view, edit, or modify the threat score but the user cannot either create a new rule or delete the predefined threat scoring rule.
    -   The changes will apply for any new observables or updates to the observables from that point onwards. To restate historical scores, they should use the recalculate option.
3.  On the form, the following fields contains the predefined values.

<table id="table_mhk_bd3_pyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the threat scoring value. For example, Threat Score Calculator.

</td></tr><tr><td>

Description

</td><td>

Description of the threat score record. For example, Calculates threat score based on weighted sum of predefined criteria scores.

</td></tr><tr><td>

Overall weightage \(Applicable to criteria builder\)

</td><td>

This field is not editable and displays the overall weightage calculated by the system based on the weight corresponding to enabled criteria.

</td></tr><tr><td>

Scoring Critera

</td><td>

Indicates the scoring criteria for an observable.Following are the two available options to define the threat scoring criteria:

-   **Criteria Builder**:

Use this option to add, edit, or remove, and enable and disable criteria that contributes to threat score calculation and ensure that the total aggregated weightage is 100%.

-   **Use Script \(Advanced\)**: The scripting feature is an advanced feature to build a custom script that should return the threat score within the range of 0-100.


</td></tr></tbody>
</table>    Below are the available options for defining the **Scoring Criteria**:

    -   Criteria Builder
    -   Use Script \(Advanced\)
    Following is the procedure for Criteria Builder:

    **Note:** You can edit or modify the existing criteria or add a new criteria.

    1.  Select the type of criteria.

        For example, Add a New Criteria.

    2.  Select the **Table** for which the criteria is configured.

        The list of values in the drop down list are Observables, Threat Actor, Campaign, Location, Identity, Vulnerability, Threat Event, Security Incident, and Aggregates. When you select one of these options from the drop down list, a condition is applied. This condition ensures that only records related to the selected value are displayed or calculated.

        **Note:**

        -   If the selected Observable, then the condition will be applied on the observable record for which the threat score will be calculated. If the selected table is not Observable, the condition will be applied only if the records are related to the Observable for which the threat score will be calculated.
        -   An additional Aggregates table is added to define the scores based on the number of relations that are associated to the Observables. For example, select the Table: Aggregates and the field value: Threat Actors then for an observable, if there are more than two threat actors, then, set the score and apply the conditions as applicable.
        -   For example, if you want to set a score for one or more threat actors associated to an observable, then, select the field as No of Threat Actors and set the desired score and apply the conditions as applicable.
    3.  Select the **Field** from the above selected table.

    4.  Enter the **Weightage** of the criteria between 0-100.

        The overall weightage of all the criteria should be 100%.

    5.  Enter the name and short description of the criteria.

    6.  Select the **Enable scoring criteria** check box to enable the scoring criteria.

    7.  Define the **Conditions** and set the score for the conditions.

    8.  You can also add new conditions using **New Condition** button, and delete the condition using the **Delete Criteria** icon.

    9.  Click **Add** to add the criteria configured.

    Here is an example of defining a condition to a threat score:

    ```
    Table: Vulnerability
    
    Field: CVSS2.0
    
    Weightage: 30%
    
    Condition-1: CVSS2.0 > 7, Score = 80
    
    Condition-2: CVSS2.0 > 4 AND CVSS2.0 < 7, Score = 50
    
    Condition-3: CVSS2.0 < 4, Score = 10
    ```

4.  Click **Re-Calculate History** button to re-caculate the threat score.

    If there are changes to the threat scoring rule then you must re apply the scoring rule to the observables which has the threat score already calculated in the past, use **Re-calculate history** button to trigger the re-calculation job.

    **Note:**

    -   A confirmation message is displayed for you to perform the action, `This is long running process that runs in the background. You won’t be able to make changes until the process is completed. Are you sure you want to run this action?`
    -   For any update events that are generating for observables as part of **Re-calculate History**, the processing of webhooks is disabled and in case if you want to enable then modify this system property `webhook_ignore_threat_score_reapply`.
5.  Click **Ok**.

    **Important:** This action will trigger a long running job and the system will not allow you to make any further changes to the threat scoring rule until the job completes. For more information on how background job configuration is configured, see [Vulnerability Response background job framework configuration](https://servicenow.com/docs/bundle/vancouver-security-management/page/product/vulnerability-response/concept/vr-background-framework.html).

    The following is the **Use Script \(Advanced\)** script: Use this script to build a custom script that should return the threat score within the range of 0-100.

    The advanced script field is auto populated with a function which takes the parameters **current** and **aggregates** and this function should return the threat score in the range of 0-100.

    Here, the current parameter is the GlideRecord object of the entity \(observable\) for which the threat score is being calculated. For the observables, it corresponds to the GlideRecord for the sn\_sec\_tisc\_observable table. The aggregates parameter is a GlideRecord object of the sn\_sec\_tisc\_aggregates table record which is used to access the record counts of the various associated record types \(such as campaigns or identities\) to the main entity \(observable\).

    Sample example of the script in the advanced option:

    ```
    answer = (function threatScoreCalculator(current, aggregates) {
     
        // return the threat score in the range of 0-100
        var threatSeverity = current.getValue("threat_severity");
        if(threatSeverity == "high")
    	    return 80;
        else {
            let associatedCampaigns = aggregates.getValue("num_of_campaigns");
            if(associatedCampaigns > 0)
                return 50;
        }
        return 0;
     
    })(current, aggregates);
    ```

    For your reference, below is the screenshot that shows you the threat score background job configuration process.

    ![Background job configuration for a threat scoring rule](../image/tisc-threat-score-vr-background-job-schedule.png)


**Parent Topic:**[Custom Threat Score Calculator in TISC](../concept/using-custom-threat-score-calculator.md)

