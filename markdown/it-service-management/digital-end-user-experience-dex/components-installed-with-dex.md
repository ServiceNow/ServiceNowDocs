---
title: Installed with DEX
description: Several types of components are installed with activation of the DEX application \[sn\_dex\] plugin, including user roles and tables.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Installed with DEX

Several types of components are installed with activation of the DEX application \[sn\_dex\] plugin, including user roles and tables.

## Roles installed

<table id="table_gvc_l53_dxb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

DEX administrator \[sn\_dex.admin\]

</td><td>

Responsible for managing user access to DEX, managing the applications that are being monitored, and handling onboarding/offboarding-related tasks. They also troubleshoot any issues that arise within the application.

</td><td>

-   agent\_client\_collector\_admin
-   report\_admin
-   sn\_dex.user
-   sn\_dex.engineer
-   sn\_cmdb\_editor

</td></tr><tr><td>

DEX engineer \[sn\_dex.engineer\]

</td><td>

Responsible for accessing and executing the remedial actions.

</td><td>

sn\_dex.user

</td></tr><tr><td>

DEX user \[sn\_dex.user\]

</td><td>

Responsible for accessing and using the features provided by DEX.

</td><td>

-   agent\_client\_collector\_user
-   cmdb\_read
-   dependency\_views
-   mbplus\_reader
-   sam\_user
-   sn\_cmdb\_editor
-   sn\_incident\_read
-   sn\_sow.sow\_home
-   sn\_sow.sow\_list
-   sn\_sow.sow\_user

</td></tr><tr><td>

DEX Service Desk agent\[sn\_dex.service\_desk\_user\]

</td><td>

Responsible for L1 or L2 support representatives accessing DEX from the incident platform to explore and investigate the details of the devices linked to the incident.

</td><td>

Not applicable

</td></tr></tbody>
</table>## Tables installed

<table id="table_kvc_l53_dxb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DEX Application\[dex\_application\]

</td><td>

Parent table that stores a list of all the applications configured for monitoring on the **Administration** &gt; **Applications** page. The table extends the parent table sn\_acc\_vis\_content\_application in the Agent Client Collector for Visibility - Content scoped app.

</td></tr><tr><td>

Metric Rules\[dex\_metric\_rules\]

</td><td>

Table that stores all the DEX metric rules.

</td></tr><tr><td>

Alert Metadata\[dex\_alert\_metadata\]

</td><td>

Table that stores data about incoming events from the metric rules.

</td></tr><tr><td>

Alert Impacted Users\[dex\_alert\_impacted\_users\]

</td><td>

Table that stores data about users or devices, which are impacted for a given metric rule.

</td></tr><tr><td>

Alert Locations\[dex\_alert\_location\]

</td><td>

Table that stores data about locations, which are impacted for a given metric rule.

</td></tr><tr><td>

Action App Config\[dex\_action\_app\_config\]

</td><td>

Table that stores applications, which support the clear app cache action.

</td></tr><tr><td>

CI Device Configuration\[dex\_ci\_device\_config\]

</td><td>

Table that stores the device configuration data including the logged-in user information.For information on the related policies and check definitions, see [DEX Content Playbook reference](dex-content-playbook-reference.md).

</td></tr></tbody>
</table>**Parent Topic:**[DEX Application and Device Health reference](dex-console-reference.md)

