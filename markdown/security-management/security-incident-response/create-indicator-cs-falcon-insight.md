---
title: Create indicators
description: Create and manage threat indicators that synchronize directly with CrowdStrike Falcon Insight, enabling consistent, up‑to‑date threat intelligence across your security environment.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-02-10"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create indicators

Create and manage threat indicators that synchronize directly with CrowdStrike Falcon Insight, enabling consistent, up‑to‑date threat intelligence across your security environment.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that contains the observables for which you want to create indicators in CrowdStrike Falcon Insight.

3.  Select **Associated Observables** related lists.

4.  Select the observables.

5.  From the **Actions** on selected rows, select **Create Indicator in CrowdStrike**.

6.  On the form, fill in the fields.

<table id="table_z2k_d5w_3sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Selected Observables

</td><td>

Observables that are affected. This action can be used to create indicators for multiple observables.**Note:** Indicators won't be created in CrowdStrike if the supported observable types are not mapped. Supported observable types include:

-   **Domain**
-   **MD5**
-   **SHA-256**
-   **IPv4**
-   **IPv6**


</td></tr><tr><td>

Source

</td><td>

Integration profile configuration used to create the indicator.

</td></tr><tr><td>

Description

</td><td>

Purpose of the indicator.

</td></tr><tr><td>

Platforms

</td><td>

Platforms where this indicator applies. Options include:-   **Windows**
-   **Mac**
-   **Linux**
-   **Android**
-   **iOS**


</td></tr><tr><td>

Action

</td><td>

Actions to be performed when the Indicator is discovered in the organization. Options include:-   **Detect**
-   **Prevent \(hash only\)**
-   **Prevent \(hidden UI\) \(hash only\)**
-   **Allow \(hash only\)**
-   **No Action**


</td></tr><tr><td>

Mobile Action

</td><td>

Action applied on supported mobile platforms. Options include:-   **Detect**
-   **Prevent \(hash only\)**
-   **Allow \(hash only\)**
-   **No Action**


</td></tr><tr><td>

Severity

</td><td>

Severity assigned to the Indicator. Options include:-   **Low**
-   **Medium**
-   **High**
-   **Critical**


</td></tr><tr><td>

Expiration

</td><td>

Date and time when the indicator will automatically expire

</td></tr><tr><td>

Tags

</td><td>

Custom label to categorize/group indicators.

</td></tr><tr><td>

Apply Globally

</td><td>

Option to apply indicator to all the hosts.When cleared, the configuration applies only to selected host groups.

</td></tr><tr><td>

Host Groups

</td><td>

Specify which CrowdStrike host groups should receive this configuration.

</td></tr></tbody>
</table>7.  Select **Create Indicator**

8.  Validate the activity and UI messages.

9.  Select **CrowdStrike Indicator** tab to view the results.


