---
title: Tracing systems in Emergency Exposure Management
description: A tracing system configured for a contact tracing data source enables you to identify potentially exposed employees by running a diagnostic request.
locale: en-US
release: yokohama
product: Emergency Exposure Management
classification: emergency-exposure-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Set up Emergency Exposure Management, Emergency Exposure Management, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Tracing systems in Emergency Exposure Management

A tracing system configured for a contact tracing data source enables you to identify potentially exposed employees by running a diagnostic request.

The diagnostic request for an affected employee queries the contact tracing data to identify people who might have interacted with the affected employee. You can select multiple tracing systems in a diagnostic request to use multiple data sources to broaden the coverage used to find potential exposure.

A tracing system can be a group of other tracing systems with a similar type of input data source. For example, say you have Wi-Fi access data integration with multiple systems such as Cisco DNA Spaces and Mist Systems. You could have a tracing system called Wi-Fi access log and make it the parent tracing system of other tracing systems using the Wi-Fi input data sources.

You can customize the tracing systems for data sources available in Emergency Exposure Management or set up a new tracing system. For more information, see [Set up a tracing system for an exposure data source](../task/set-up-tracing-system.md).

For some tracing systems to be available in Emergency Exposure Management, you must install other Safe Workplace suite and Emergency Response Operations applications.

## Tracing systems installed with Emergency Exposure Management

These tracing systems are active by default.

<table id="table_sgm_ndx_cmb"><thead><tr><th>

Tracing system

</th><th>

Query

</th></tr></thead><tbody><tr><td>

**Location**

</td><td>

Employees co-located with the affected employee, for example, on the same floor or building.

</td></tr><tr><td>

**Outlook meetings** Microsoft Office 365

</td><td>

Employees who accepted the same meetings as the affected employee during the specified time period.

</td></tr></tbody>
</table>## Tracing system installed with Workplace Core

This tracing system is not active by default. To use this tracing system for identifying potentially exposed employees, activate it and also configure the corresponding data source in Workplace Core.

For more information, see [Install Workplace Safety Management](../../workplace-safety-mgmt/task/install-workplace-safety-mgmt-hr.md).

|Tracing system|Query|
|--------------|-----|
|**Workplace reservations**|Employees who had reservations for the same shifts as the affected employee during the specified time period.|

## Tracing systems installed with Contact Tracing

These tracing systems are not active by default. To use these tracing systems for identifying potentially exposed employees, activate them and also configure the corresponding data sources in Contact Tracing.

For more information, see [Setting up Contact Tracing](../../contact-tracing/concept/set-up-contact-tracing.md).

<table id="table_q3t_nt2_bnb"><thead><tr><th>

Tracing system

</th><th>

Query

</th></tr></thead><tbody><tr><td>

**Badge reader**

</td><td>

Queries the Badge Access Register \[sn\_imt\_tracing\_badge\_access\_register\] table to fetch employees who swiped their badge on the same badge reader devices as the affected employee during the specified time period.

</td></tr><tr><td>

**Employee daily log**

</td><td>

Queries the Daily Contact Logs \[sn\_imt\_tracing\_daily\_contact\_log\] table to fetch employees with whom the affected employee interacted during the specified time period.

</td></tr><tr><td>

**Visitor log**

</td><td>

Queries the Visitor Request For Entry \[sn\_imt\_monitoring\_visitor\_request\_for\_entry\] table to fetch visitors who interacted with the affected employee during the specified time period. Visitors who visited the workplace on invitation from the affected employee and have been screened through and let in are queried.Ensure that you have installed Employee Health Screening to use this tracing system.

</td></tr><tr><td>

**Wi-Fi access log**

</td><td>

Queries the Wi-Fi Access Register \[sn\_imt\_tracing\_wifi\_access\_register\] table to fetch employees who used the same Wi-Fi access points as the affected employee during the specified dates.Wi-Fi access log data used to identify potentially impacted employees depends on Wi-Fi location preferences and available integrations. The tracing system has the following child tracing systems based on the data source:

-   Mist Systems
-   Cisco DNA Spaces

 For more information, see [Retrieving Wi-Fi access log data](../../contact-tracing/concept/wifi-access-management.md).

 **Note:** The period for which you can get the data via a real-time API depends on the data retention policy of your Wi-Fi service provider.

</td></tr><tr><td>

**Handheld/Wearables**

</td><td>

Queries the Wearable Access Register \[sn\_imt\_tracing\_wearable\_access\_register\] table to fetch employees equipped with handheld or wearable devices who were in the close proximity with the affected employee during the specified time period. The Handheld/Wearables tracing system has the Zebra MotionWorks Proximity tracing system added as a child tracing system.

</td></tr><tr><td>

**Kinexon SafeZone**

</td><td>

Uses an integration with the KINEXON SafeZone API to identify potentially exposed users with KINEXON wearable devices who were in close proximity with the affected KINEXON user during the specified dates.For more information, see [Configure KINEXON integration](../../contact-tracing/task/configure-kinexon-integration.md).

</td></tr></tbody>
</table>## Tracing system installed with Field Service Management

This tracing system is not active by default. To use this tracing system for identifying potentially exposed employees, activate it and also configure the corresponding data source in Field Service Management.

For more information, see [Emergency Exposure Management for field service agents](https://www.servicenow.com/docs/access?context=monitoring-analytics-fsm&version=yokohama&pubname=yokohama-field-service-management&section=exposure-management-for-agents&ft:locale=en-US).

|Tracing system|Query|
|--------------|-----|
|**Field service**|Customers attended by an affected field agent during the specified time period. Also queries other field agents who interacted with the affected agent or visited the same customer as the affected agent during the specified time period.|

