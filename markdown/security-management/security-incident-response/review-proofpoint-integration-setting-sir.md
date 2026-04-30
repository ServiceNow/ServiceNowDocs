---
title: Review Proofpoint integration settings
description: Review the Proofpoint integration settings so that you can modify the system properties for your environment.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Proofpoint Integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Review Proofpoint integration settings

Review the Proofpoint integration settings so that you can modify the system properties for your environment.

## Before you begin

Role required: sn\_si\_admin

## Procedure

1.  Navigate to **All** &gt; **SIR Integration with Proofpoint** &gt; **Proofpoint Integration Settings**.

2.  Modify the following settings.

<table id="table_hcf_3z4_c2c"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TimeOut for the restAPI calls.sn\_sec\_proofpoint.http\_timeout

</td><td>

The timeout \(in seconds\) for fetching data from the api calls.Type: Integer

Default value: 3000

</td></tr><tr><td>

Logging level - debug, info, warn, errorsn\_sec\_proofpoint.logging\_verbosity

</td><td>

The log verbosity level of the application, meaning the name of the type of information. You can update the value to the following options:-   error
-   warn
-   info
-   debug
Default value: info

</td></tr><tr><td>

Enforce a limit on number of Proofpoint Events that can be aggregated to a single incident.sn\_sec\_proofpoint.max\_aggregations\_per\_si

</td><td>

The maximum number of Proofpoint events that can be aggregated to one incident.Type: Integer

Default value: 100

</td></tr><tr><td>

Enforce a limit on number of security incidents that can be created in 24 hour period.sn\_sec\_proofpoint.max\_si\_per\_day

</td><td>

The maximum number of incidents that can be created in 24 hours.Type: Integer

Default value: 1000

</td></tr><tr><td>

No of days, we need to use in api call for top clickers, vap.sn\_sec\_proofpoint.default\_days

</td><td>

The number of days of data to fetch for top clickers and VAP. You can also update the value to the following options:-   14
-   30
-   90
Type: Integer

Default value: 90

</td></tr><tr><td>

Boolean flag, if enabled it makes api call and populates Topclickers details.sn\_sec\_proofpoint.call\_topclickers\_api

</td><td>

Activate the option to enable and fetch top clicker data.Type: Boolean

Default value: True

</td></tr><tr><td>

Boolean flag, if enabled it makes api call and populates VAP details.sn\_sec\_proofpoint.call\_vap\_api

</td><td>

Activate the option to enable and fetch VAP data.Type: Boolean

Default value: False

</td></tr><tr><td>

It is to restrict the maximum number of users to display for topClickers, VAP Users.sn\_sec\_proofpoint.maxresults

</td><td>

The maximum number of users to display for top clickers and VAP users.Type: Integer

Default value: 100

</td></tr><tr><td>

Enables/Disables using overlapping period during scheduled polling of Proofpoint Events.sn\_sec\_proofpoint.allow\_overlap

</td><td>

Enable or disable overlapping period when scheduled polling is configured.Type: Boolean

Default value: False

</td></tr><tr><td>

Overlap time in minutes to be used during scheduled polling of ProofpointEvents when overlap is enabled.sn\_sec\_proofpoint.overlap\_time

</td><td>

The overlap time in minutes when scheduled polling is configured.Type: Integer

Default value: 5

</td></tr></tbody>
</table>3.  Select **Save**.


## Result

Configures the integration settings with new values.

