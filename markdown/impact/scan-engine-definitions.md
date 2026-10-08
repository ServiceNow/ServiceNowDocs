---
title: Scan Engine definitions
description: The Scan Engine uses a large set of definitions to correct coding and workflow findings in real-time and perform scans across your entire instance to detect existing findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/scan-engine-definitions.html
release: brazil
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 2
breadcrumb: [Scan Engine reference, Impact reference, Impact]
---

# Scan Engine definitions

The Scan Engine uses a large set of definitions to correct coding and workflow findings in real-time and perform scans across your entire instance to detect existing findings.

## Pre-defined definitions

There are various types of definitions available as a baseline in the Impact Scan Engine. Category weighting reflects how much risk each area typically represents across the check library. These weights are applied only at the final roll-up step, so a change in one category's findings won't distort the calculated health of another category.

<table id="table_zby_my2_m2c"><thead><tr><th>

Category

</th><th>

Weight

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Security

</td><td>

-   ~40%
-   The highest-consequence category, encompassing breach risk, compliance violations, and access-control vulnerabilities.

</td><td>

Measures implementation of protocols across a ServiceNow instance to prevent unauthorized access, data breaches, cyber attacks, and potential vulnerabilities.

</td></tr><tr><td>

Performance

</td><td>

-   ~22%
-   Affects every user on the instance and compounds if left unaddressed.

</td><td>

Measures the efficiency of a ServiceNow instance, encompassing aspects such as speed, responsiveness, resource utilization, and overall dependability.

</td></tr><tr><td>

Manageability

</td><td>

-   ~19%
-   The largest category by volume, impacting administration and supportability.

</td><td>

Measures the extent to which ServiceNow instances, applications, or infrastructure can be effectively monitored, configured, and maintained.

</td></tr><tr><td>

Upgradeability

</td><td>

-   ~9%
-   Smaller in volume, but can block or delay version upgrades.

</td><td>

Assesses the ease of enhancing a ServiceNow instance or application with new features, improvements, security patches, or compatibility adjustments.

</td></tr><tr><td>

User Experience

</td><td>

-   ~9%
-   Important to adoption and satisfaction, but carries the lowest urgency overall.

</td><td>

Evaluates the quality of user interactions with applications. Considers the ease of use, efficiency, design, responsiveness, accessibility, and its emotional and functional impact.

</td></tr></tbody>
</table>**Note:** For a complete explanation of how these weights are applied in your overall Instance Health Score calculation, see [Platform Health score calculation model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-health-score-calculation.md).

## Custom definitions

Users can create their own custom definitions. For more information, see [Create custom Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/create-scan-engine-definitions.md).

**Note:** The number of custom definitions that is permitted varies based on your Impact package. For more information, see [Impact packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-packages1.md).

## Scan Engine definition suites

Definition suites are groupings of similar definitions that allow administrators to target specific areas or functions of code during scans.

For more information, see [Customize Scan Engine definition suites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/create-scan-engine-definition-suites.md).

**Parent Topic:**[Scan Engine reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-reference.md)

