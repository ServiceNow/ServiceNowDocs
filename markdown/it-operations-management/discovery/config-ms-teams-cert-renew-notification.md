---
title: Complete certificate renewal in Servicenow
description: You can renew a certificate directly from a Microsoft Teams message sent autoamticaly by your ServiceNow patform.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "0256-02-16"
reading_time_minutes: 1
breadcrumb: [Configure for MS Teams Integration, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Complete certificate renewal in Servicenow

You can renew a certificate directly from a Microsoft Teams message sent autoamticaly by your ServiceNow patform.

## Before you begin

Configure your MS Teams for Certificate Inventory and Management integration. For more information, see [https://www.servicenow.com/docs/r/integrate-applications/integration-hub/set-up-msteams.html](https://www.servicenow.com/docs/r/integrate-applications/integration-hub/set-up-msteams.html). Configure your Certificate Inventory and Management system to send notifications to Microsoft Teams and the channel you want to receive them. For more information, see [Configure for MS Teams Integration](cim-ms-teams-integration.md).

You need a CSR or auto renewal configured. For more information, see [Configuring automated certificate renewal](../../it-operations-management/concept/configuring-automated-certificate-renewal.md).

Role required: pki\_admin or admin

## Procedure

1.  Select **Renew Certificate in Servicenow in your MS Teams notification message.**

2.  In the form that follows, fill out the following fields

<table><tbody><tr><td id="d459624e98">

**Field**

</td><td>

Value

</td></tr><tr><td id="d459624e107">

**Choose how you want to provide CSR**

</td><td>

Manually \| Auto generate with private key

</td></tr><tr><td id="d459624e116">

**Validity period in days**

</td><td>

Number of days

</td></tr><tr><td id="d459624e125">

**Certificate Signing Request \(CSR\)**

</td><td>

Your CSR

</td></tr></tbody>
</table>3.  Select **Submit**.


