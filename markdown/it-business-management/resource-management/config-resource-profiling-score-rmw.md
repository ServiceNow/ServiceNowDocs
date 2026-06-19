---
title: Configure resource profiling score
description: Configure the resource profiling score to adjust how the AI Resource Finder ranks candidates by modifying attribute weights in the CandidateProfileScoringConfigSNC script include.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/resource-management/config-resource-profiling-score-rmw.html
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Configure, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure resource profiling score

Configure the resource profiling score to adjust how the AI Resource Finder ranks candidates by modifying attribute weights in the CandidateProfileScoringConfigSNC script include.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Locate and open the **CandidateProfileScoringConfigSNC** script include record.

3.  To edit the record change the scope of the application to SPM Planning Attributes.

4.  Use the Script field to view and understand the current allocation logic using the `getWeights` function.

    Following is the default code.

    ```
    var CandidateProfileScoringConfigCustom = Class.create();
        CandidateProfileScoringConfigCustom.prototype = Object.extendsObject(
            CandidateProfileScoringConfigSNC, {
    
            getWeights: function() {
                return {
                    availabilityCoverage: 0.40,
                    attrExpScore:         0.20,
                    prjExpScore:          0.20,
                    adjacentAttrExp:      0.15,
                    generalExp:           0.05
                };
            },
    
            type: 'CandidateProfileScoringConfigCustom'
        });
    ```

<table id="table_azn_3p2_njc"><thead><tr><th>

Attributes

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

availabilityCoverage

</td><td>

Scoring attribute indicating resource's as capacity during the assignment period.This is the dominant factor. A resource with perfect skills but no availability scores lower than a less experienced resource who is free when needed.

</td></tr><tr><td>

attrExpScore

</td><td>

Whether the resource has worked with the same planning attributes \(such as role or skills group\) that the assignment requires.

</td></tr><tr><td>

prjExpScore

</td><td>

Scoring indicating if resource has worked on similar projects before.

</td></tr><tr><td>

adjacentAttrExp

</td><td>

Whether the resource has experience with related planning attributes, but not identical ones. For example, a Developer considered for a Senior Developer assignment.

</td></tr><tr><td>

generalExp

</td><td>

The resource's overall organizational tenure and breadth of work history.

</td></tr></tbody>
</table>5.  Edit the allocation of the existing attributes to match with your organization requirements.

6.  Verify that the five values add up to 1.0, indicating 100%.

7.  Select **Submit**.


## Result

The AI Resource Finder uses the custom weights for subsequent fit score calculations. Resources are re-ranked according to the new weight distribution the next time a user opens the Resource Finder modal.

**Parent Topic:**[Configure Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/configure-rmw.md)

