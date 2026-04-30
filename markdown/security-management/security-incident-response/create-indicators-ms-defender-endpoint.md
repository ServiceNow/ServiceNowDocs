---
title: Create indicators in Microsoft Defender for Endpoint
description: Create indicators from associated observables of the security incident using the Microsoft Defender for Endpoint.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create indicators in Microsoft Defender for Endpoint

Create indicators from associated observables of the security incident using the Microsoft Defender for Endpoint.

## Before you begin

Role required: sn\_si.admin, sn\_si.analyst

## About this task

The Microsoft Defender for Endpoint integration allows observable enrichment for all the observable types that are mapped in the Observable-Indicator mapping module.

Create indicators provide you the ability to set a list of indicators for detection, and for blocking prevention and responses. You can create the indicators from associated observable of the security incident.

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that contains the observables for which you want to create indicators in Microsoft Defender for Endpoint.

3.  Click the Associated Observables related lists.

4.  Add any existing observables or create new observables.

5.  Select the observables.

6.  From the **Actions** on selected rows, click **Create Indicator in Microsoft Defender**.

    ![Associated Deliverables view: Select Create Indicators in Microsoft Defender for Endpoint from the Actions list.](../image/create_indicators.png)

7.  On the form, fill in the fields.

<table id="table_z2k_d5w_3sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Selected Observables

</td><td>

Observables that are affected. This action can be used to create indicators for multiple observables. If you want to deselect an observable, you can do that by deselecting the observables from the list.**Note:** If the supported observable types are not mapped, then the indicators are not created in the Microsoft Defender for such observables.

</td></tr><tr><td>

Title

</td><td>

Title for the indicator.

</td></tr><tr><td>

Description

</td><td>

Description for the indicator.

</td></tr><tr><td>

Expiration Time

</td><td>

Expiration time for the indicator.

</td></tr><tr><td>

Recommended Actions

</td><td>

Recommended actions that must be performed for the indicator.

</td></tr><tr><td>

Source

</td><td>

Integration configuration to create the indicator.

</td></tr><tr><td>

Action

</td><td>

Actions that will be performed if the Indicator is discovered in the organization. The possible values are as follows: -   **Warn**
-   **Block**
-   **Audit**
-   **'BlockAndRemediate**
-   **Allowed**


</td></tr><tr><td>

Application

</td><td>

The Microsoft Defender for Endpoint application that is associated with the indicator. This field is applicable only for a new indicator and cannot be used for an existing indicator.

</td></tr><tr><td>

Severity

</td><td>

Severity of the Indicator. The possible values are as follows:-   **Low**
-   **Medium**
-   **High**


</td></tr><tr><td>

RBAC Group Names

</td><td>

RBAC group names that the indicator would be applied to. The names are in a comma-separated list.

</td></tr></tbody>
</table>8.  Click **Create Indicator**

9.  Validate the activity and UI messages.

10. Click the **Microsoft Defender Indicator** tab to view the results.


