---
title: DEX Score survey configuration form
description: Update the configuration for sending the surveys to collect feedback from employees on the usage of applications and devices.
locale: en-US
release: zurich
product: Digital Experience Score
classification: digital-experience-score
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Digital Experience Score, Digital End-User Experience, IT Service Management]
---

# DEX Score survey configuration form

Update the configuration for sending the surveys to collect feedback from employees on the usage of applications and devices.

For more information, see [Update DEX Score survey configuration](../task/dexscr-set-survey-config.md).

<table id="table_wdl_bcc_lyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Survey feedback type

</td><td>

Type of the survey to determine whether it's for collecting feedback on the application or device experience.

</td></tr><tr><td>

Survey trigger group

</td><td>

Recipients of the survey. The default value is **Random group every week**.

</td></tr><tr><td>

Repeat survey after

</td><td>

Period after which the survey can be sent again to the same recipient group.

</td></tr><tr><td>

Active from

</td><td>

Date from which the survey is effective and will be sent to the specified recipients group.

</td></tr><tr><td>

Active

</td><td>

Option to make the survey configuration active.

</td></tr><tr><td>

Trigger criteria

</td><td>

Criteria to trigger the survey.This field appears only when **Application** is selected from**Survey feedback type**.

</td></tr><tr><td>

Minimum threshold \(per week\)

</td><td>

Minimum threshold value for the trigger criteria so that the survey is triggered and sent to the recipients.For example, if the trigger criterion is application usage time and the minimum threshold is set to 15 \(hours per week\), then the survey is sent to only the recipients who used the application for more than 15 hours in a particular week.

This field appears only when **Application** is selected from**Survey feedback type**.

</td></tr></tbody>
</table>**Parent Topic:**[Digital Experience Score​ reference](../concept/dexscr-dex-score-reference.md)

