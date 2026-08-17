---
title: System properties for AI asset security
description: System properties that connect Veza access intelligence and limit the age of records evaluated for AI asset security metrics are available. Limiting records can prevent analyzing stale data and reduce unnecessary processing overhead.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-sec-reference-system-properties.html
release: zurich
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# System properties for AI asset security

System properties that connect Veza access intelligence and limit the age of records evaluated for AI asset security metrics are available. Limiting records can prevent analyzing stale data and reduce unnecessary processing overhead.

Properties exist in the System Properties \[sys\_properties\] table. The admin role is necessary to set system properties.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ai\_security.analyzer\_max\_record\_age\_hours

</td><td>

Limit by record age \(in hours\) the number of AI asset invocation records processed by AI Control Tower for AI asset security metrics. Reducing the record age can prevent analyzing stale data, reduce unnecessary processing overhead, and focus the metric on more recent activity. Increasing the record age includes analysis of older records.

 -   Type: Integer
-   Default value: 4 hours
-   Location: The System Properties \[sys\_properties\] table

</td></tr><tr><td>

sn\_ai\_security.veza.api.key

</td><td>

The Veza API access token that controls authentication for data for access intelligence. For more information, see [Configure Veza access intelligence in the agent map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-veza-access-intelligence.md).-   Type: password2
-   Default value: false
-   Location: The System Properties \[sys\_properties\] table

</td></tr><tr><td>

sn\_ai\_security.veza.api.url

</td><td>

The base URL of the Veza tenant that provides access intelligence data for the agent map. For example, `https://your-tenant.vezacloud.com`. For more information, see [Configure Veza access intelligence in the agent map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-veza-access-intelligence.md).-   Type: string
-   Default value: false
-   Location: The System Properties \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Managing AI asset security reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-reference.md)

