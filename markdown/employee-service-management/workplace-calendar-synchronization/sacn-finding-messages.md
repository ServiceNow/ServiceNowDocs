---
title: Instance scan findings
description: After the instance scan completes, on the Scan Result form, review the findings in the Scan Findings related list.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workplace Calendar Synchronization references, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Instance scan findings

After the instance scan completes, on the Scan Result form, review the findings in the Scan Findings related list.

## Scan findings

The following findings are reported in the scan report:

-   `Could not find the sn_ex_online_spke.Microsoft_Exchange_Online Connection and credential alias.`
-   `The Connection & credential alias specified in the Override alias is not a child alias to the sn_ex_online_spke.Microsoft_Exchange_Online Connection and credential alias.`
-   `There are multiple/no connections associated with the ' + selectedAlias.getValue('name') + ' Connection and credential alias.`
-   `There are multiple/no connection attributes associated with ' + selectedAlias.getValue('name') + ' Connection and credential alias.`
-   `Incorrect 'Connection URL' specified in the " + selectedAlias.getValue('name') + " Connection and credential alias."`
-   `OAuth provider associated with the OAuth Entity Scope - ' + scope + ' is not same as the one associated with OAuth Entity Profile of this scope.`
-   `The OAuth Scope - ' + scopesExpected[i] + ' must be associated with the grant type ' + grantType + '.`
-   `The Default grant type of the OAuth provider must be same as the Grant type of the OAuth Entity Profile.'`
-   `OAuth Token has expired.`
-   `Please generate an OAuth Token.`
-   `Invalid token URL associated with Application Registry - ' + applicationRegistryGr.getValue('name') + '.`
-   `Invalid authorization URL associated with Application Registry - ' + applicationRegistryGr.getValue('name') + '.`
-   `Invalid redirect URL associated with Application Registry - ' + applicationRegistryGr.getValue('name') + '.`
-   `There is no OAuth Entity Profile associated with the credential - ' + credentialGr.getValue('name') + '.`
-   `There is no credential associated with the connection - ' + connectionGr.getValue('name') + '.`
-   `There is no active credential associated with the connection - ' + connectionGr.getValue('name') + '.`
-   `Invalid Credential record associated with connection - ' + connectionGr.getValue('name') + '.`
-   `If the grant type of the connection (linked with provider) is set as Authorization Code, the provider must have Strict mode enabled with a valid Strict mode email.`
-   `Synchronization is not configured - could not find an active provider.`
-   `There are multiple subscriptions associated with this resource.`
-   `Calendar provider associated with this Rsv Sync Configuration is inactive.`
-   `Could not find an email with this Rsv Sync configuration.`
-   `The Rsv Sync configuration email must be same as the email specified in the 'Email' field of the location record.`
-   `The same email is associated with a different Rsv sync configuration.`
-   `The Subscription has expired.`
-   `The Subscription status is ' + status + '.`
-   `Invalid Subscription.`
-   `Could not find a subscription for this Rsv Sync Configuration.`

To fix a finding, refer to the following:

-   [Microsoft Exchange Online - Calendar synchronization](ms-exchange-reservation-synchronization.md)
-   [Synchronization - Prerequisites and implementation](synchronization-troubleshooting-and-conditions.md)

**Parent Topic:**[Workplace Calendar Synchronization references](../concept/workplace-calendar-sync-references.md)

**Related topics**  


[Components installed with Workplace Calendar Synchronization](components-installed-with-workplace-calendar-syncn.md)

[Properties installed with Workplace Calendar Synchronization](properties-installed-with-workplace-calendar-syncn.md)

[Scheduled jobs installed with Workplace Calendar Synchronization](scheduled-jobs-installed-with-workplace-calendar-synchronization.md)

[Flows installed with Workplace Calendar Synchronization](flows-installed-with-workplace-calendar-synchronization.md)

