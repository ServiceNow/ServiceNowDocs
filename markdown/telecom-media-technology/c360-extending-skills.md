---
title: Extend the Telecommunications Customer 360 Insights
description: Extend the Telecommunications Customer 360 summary card by registering a new ServiceNow Otto skill with the orchestrator quick action and adding it to the merge order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/c360-extending-skills.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Extend the Telecommunications Customer 360 Insights

Extend the Telecommunications Customer 360 summary card by registering a new ServiceNow Otto skill with the orchestrator quick action and adding it to the merge order.

## About this task

Telecommunications Customer 360 Insights combines multiple ServiceNow Otto skills into a single insight card. The **Generate telecom customer 360 insights** quick action runs all registered skills and merges their outputs into a single summary displayed in the ServiceNow Otto panel. By default, the following skills are included:

-   Top Issues
-   Health &amp; Sentiment

**Note:** Adding a new skill requires no changes to the existing skills or the overall quick action setup.

## Before you begin

-   Role required: admin
-   Build and configure the new ServiceNow Otto skill before completing this task. Note the sys\_id values for the skill and its configuration record.

## Procedure

1.  Open the **Generate telecom customer 360 insights** quick action.

    1.  Navigate to **All** and type `Quick Actions` in the filter navigator.

    2.  Open the **Quick Actions** list.

    3.  Search for **Generate telecom customer 360 insights** and open the record.

2.  Register the new skill in the quick action script.

    1.  Open the **Script** field for editing.

    2.  Locate the `INSIGHT_SKILLS` array and add a new entry for the skill.

    Each entry in the array requires the following properties:

    -   `key` — a unique identifier for the skill, used later in the merge order.
    -   `capabilityId` — the sys\_id of the ServiceNow Otto skill record.
    -   `skillConfigId` — the sys\_id of the skill configuration record.
    -   `buildFingerprint` — a function that builds the input fingerprint used to identify and cache the skill's request.
    ```
    var INSIGHT_SKILLS = [
        {
            key: 'top_issues',
            capabilityId: 'd01605b32baa3690449af5b14391bf47',
            skillConfigId: '601605b32baa3690449af5b14391bf93',
            buildFingerprint: function(inps) {
                return fingerprintUtil.buildTopIssuesFingerprint(inps);
            }
        },
        {
            key: 'health',
            capabilityId: 'f40562b32b667690449af5b14391bf9e',
            skillConfigId: '410562b32b667690449af5b14391bff8',
            buildFingerprint: function(inps) {
                return fingerprintUtil.buildHealthFingerprint(inps);
            }
        },
        {
            key: 'contract_renewal',
            capabilityId: '<sys_id of your new ServiceNow Otto skill>',
            skillConfigId: '<sys_id of your new skill configuration>',
            buildFingerprint: function(inps) {
                return fingerprintUtil.buildContractRenewalFingerprint(inps);
            }
        }
    ];
    ```

3.  Open the **TelecomC360InsightsCallbackHandler** script include.

    1.  Navigate to **All** and type `Script Includes` in the filter navigator.

    2.  Search for **TelecomC360InsightsCallbackHandler** and open the record.

4.  Add the new skill key to the merge order array.

    Locate the line that builds the merged summary and insert the new skill's `key` value in the position where you want it to appear in the combined insight card.

    ```
    var mergedMarkdown = ['top_issues', 'health', 'contract_renewal'].map(function(k) {
        return byKey[k] && byKey[k].model_output ? byKey[k].model_output : '';
    }).filter(function(t) { return t && t.length > 0; }).join('\n\n');
    ```

    **Important:** Only keys listed in this array are included in the combined insight card. A skill whose key is missing here generates output but does not display it.

5.  Save both records.


## Result

The new ServiceNow Otto skill runs alongside the existing skills when the **Generate telecom customer 360 insights** quick action is triggered, and its output appears in the combined summary at the position you specified.

**Parent Topic:**[Configure Telecommunications Customer 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/c360-configure.md)

