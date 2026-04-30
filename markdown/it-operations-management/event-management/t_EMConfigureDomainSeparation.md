---
title: Configure Event Management domain separation
description: You can configure Event Management for domain separation to create logically defined domains that limit unauthorized access to data. When domains are separated in Event Management, users can only see and manage alerts and events in their own \(tenant\) domain.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Domain separation and Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure Event Management domain separation

You can configure Event Management for **domain separation** to create logically defined domains that limit unauthorized access to data. When domains are separated in Event Management, users can only see and manage alerts and events in their own \(tenant\) domain.

## Before you begin

Role required: evt\_mgmt\_admin and evt\_mgmt\_integration

## About this task

Activate the **Domain Support – Domain Extension Installer** plugin and configure the MID Server for Event Management.

The following Event Management features have limited domain separation support.

<table id="table_owh_2j3_f5"><thead><tr><th>

Feature

</th><th>

Support

</th></tr></thead><tbody><tr><td>

Event – alert flow

</td><td>

Supported. Separation is based on the domain user that sent events. User access is required for the credentials of the sending API events or in the configuration of the MID Server reporting events.

In a multi-domain environment, each MID Server can serve only one domain according to the integration user that it uses. In the configuration of the connector instance, make sure that the MID Server have same domain as Connector instance.

To configure pull connectors to support custom domain separation, see [Personalize domains for pull connector events to use in event creation](personalize-domain-separation-pull-connectors.md).

</td></tr><tr><td>

Impact calculation

</td><td>

Supported.Segregation is based on the manner in which CIs are segregated.

</td></tr><tr><td>

Application services

</td><td>

Partially supported. Segregation is based on the manner in which CIs are segregated.

</td></tr><tr><td>

Dynamic CI groups

</td><td>

Partially supported. Segregation is based on the manner in which CIs are segregated.

 **Note:** The discovery process does not segregate CIs by domain.

</td></tr><tr><td>

Remediation

</td><td>

Supported. While editing alert management rules, users can only apply relevant workflows.

For more information on domain separation in the Flow Designer, see [Domain separation and Flow Designer.](https://www.servicenow.com/docs/access?context=flow-designer-domain-separation&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

</td></tr><tr><td>

Alert Aggregation

</td><td>

Supported. In domain-separated environments, alert groups are created only for alerts in the same domain.

</td></tr></tbody>
</table>## Procedure

1.  If it is not already active, activate the Domain Support – Domain Extension Installer plugin.

2.  Configure the connector instance to be in the same domain as the MID Server.


