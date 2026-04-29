---
title: Configure Devvio integration
description: Configure Contact Tracing properties to import risk scores from the DevvTrace platform using the Devvio API.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Collecting risk scores in Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure Devvio integration

Configure Contact Tracing properties to import risk scores from the DevvTrace platform using the Devvio API.

## Before you begin

Ensure you have a Devvio administrator user name and password.

Role required: sn\_imt\_tracing.wearable\_admin or admin

## About this task

ServiceNow Contact Tracing integrates with the DevvTrace platform to collect user risk scores based on interactions at the workplace. To leverage risk scores from DevvTrace, your employees must be using supported wearable devices and you must have access points for Devvio.

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Administration** &gt; **Properties**.

2.  Set the Contact Tracing property values related to the Devvio integration.

<table id="table_frw_z1r_qnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_imt\_tracing.devvio.login.api.endpoint**

</td><td>

API endpoint used to log in to the Devvio instance and access DevvTrace data.

</td></tr><tr><td>

**sn\_imt\_tracing.devvio.integration.username**

</td><td>

Devvio administrator user name.

</td></tr><tr><td>

**sn\_imt\_tracing.devvio.integration.password**

</td><td>

Devvio administrator password.

</td></tr><tr><td>

**sn\_imt\_tracing.devvio.risk.report.api.endpoint**

</td><td>

Devvio Risk Report API endpoint used to fetch risk report and scores.

</td></tr><tr><td>

**sn\_imt\_tracing.devvio.risk.threshold**

</td><td>

The risk threshold value for Devvio case creation. The default value is 90.

-   If the risk score is greater than or equal to this value but less than 100, the health status is set to **Under Investigation**.
-   If the risk score is equal to 100, the health status is set to **Infected**, regardless of this value.


</td></tr></tbody>
</table>3.  Click **Save**.


## Result

The Devvio Users Risk Report updates daily at midnight \(00:00\) instance time. New cases are created when risk scores trigger Devvio case creation. For these cases, the reported source is set to **Wearable**. If a user has an open case and their risk score is greater than or equal to the risk threshold value, the case is updated and a work note is added.

**Note:** If a user with an open case has a health status other than **Cleared**, a work note is added but the source remains unchanged. If a user with an open case has a health status of **Cleared**, their health status updates to **Under Investigation** or **Infected** and a work note is added. The source for the case remains unchanged.

**Parent Topic:**[Collecting risk scores in Contact Tracing](../concept/contact-tracing-collect-risk-scores.md)

