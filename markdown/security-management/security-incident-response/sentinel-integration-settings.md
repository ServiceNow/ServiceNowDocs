---
title: Review the Microsoft Azure Sentinel integration settings
description: Review the Microsoft Azure Sentinel integration settings so that you can modify the system properties to suit your environment.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Review the Microsoft Azure Sentinel integration settings

Review the Microsoft Azure Sentinel integration settings so that you can modify the system properties to suit your environment.

## Before you begin

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  Navigate to **All** &gt; **Microsoft Azure Sentinel Integration** &gt; **Azure Sentinel Integration Settings**.

2.  Modify the following settings as required.

<table id="table_xpj_dv5_nnb"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enforce a limit on the number of days for which sample data can be fetched.sn\_sec\_sentinel.max\_num\_of\_days\_for\_sample\_data

</td><td>

Maximum number of days for which you can fetch sample data from the Microsoft Azure Sentinel environment.Type: integer

Default value: 7

</td></tr><tr><td>

Receive updates related to new alerts that are linked to SIR.sn\_sec\_sentinel.incident\_updates

</td><td>

Activate the option to receive incident updates.

Type: Boolean

Default value: True

</td></tr><tr><td>

The delimiter character to split the values in Microsoft Azure Sentinel field mappings.sn\_sec\_sentinel.delimiter

</td><td>

The delimiter character to split the values in Microsoft Azure Sentinel field mappings.Type: String

Default value: ', ' \(comma with space\)

</td></tr><tr><td>

Enforce a limit on the number of sample incidents that can be fetched.sn\_sec\_sentinel.max\_num\_of\_sample\_incident\_per\_call

</td><td>

Maximum number of sample incidents that you fetch from the Microsoft Azure Sentinel environment for ingestion.

Type: integerDefault value: 5

 Sample maximum value: 20

</td></tr><tr><td>

Enforce a limit on the number of sentinel incidents that can be aggregated to a single incident.sn\_sec\_sentinel.max\_aggregations\_per\_si

</td><td>

Incident aggregation limit for a security incident. For example, if there are 102 incidents, the first 100 are aggregated to security incident\_1 and the remaining 2 to security incident\_2.

Type: integerDefault value: 100

</td></tr><tr><td>

Enforce a limit on the number of security incidents that can be created in a 24-hour period.sn\_sec\_sentinel.max\_si\_per\_day

</td><td>

Maximum number of security incidents that can be created in a 24-hour period in the ServiceNow AI Platform.

Type: integerDefault value: 1000

</td></tr><tr><td>

Maximum pagination limit for fetching the incident data in one REST call.sn\_sec\_sentinel.max\_page\_size

</td><td>

Pagination limit for fetching the incident data in one REST call from the Microsoft Azure Sentinel environment.

Type: integerDefault value: 100

</td></tr><tr><td>

API version value for Incidents.sn\_sec\_sentinel.sentinel\_security\_incident\_api\_version

</td><td>

The Microsoft API version for retrieving Sentinel incidents.Default value: 2021-10-01

</td></tr><tr><td>

API version value for Alerts.sn\_sec\_sentinel.sentinel\_security\_alert\_api\_version

</td><td>

The Microsoft API version for retrieving Sentinel alerts.Default value: 2021-10-01

</td></tr><tr><td>

API version value for Entities.sn\_sec\_sentinel.sentinel\_security\_entities\_api\_version

</td><td>

The Microsoft API version for retrieving Sentinel entities.Default value: 2021-10-01

</td></tr><tr><td>

sn\_sec\_sentinel.logging.verbosity

</td><td>

The log verbosity level of the application, meaning the name of the type of information. You can also update the value to the following options:-   **error**
-   **warn**
-   **info**
-   **debug**
 Default value: **info**.

</td></tr></tbody>
</table>3.  Click **Save**.

    Your modified integration settings are applied in the next polling interval as defined in the profile.


