---
title: Threat Lookup Finding Calculators
description: Threat Lookup Finding Calculator helps you calculate the observable findings based on the responses received.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-lookup-finding-calculators.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Threat Intelligence administration, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Threat Lookup Finding Calculators

Threat Lookup Finding Calculator helps you calculate the observable findings based on the responses received.

You can create a Threat Lookup Finding Calculator for your integration and use a script to determine how you want to identify the various observable findings. The Threat Lookup Finding Calculator includes a sample script that comes with the base system, which you can use to identify the observable findings or you can modify this script according to your requirements.

For third-party integrations that provide the computed results, the Threat Lookup Finding Calculator maps the results to supported findings in the base system.

## Rollup Threat Lookup Results

When you have multiple threat lookup results for an observable from the various integration vendors, then the recent threat lookup results from all the vendors are considered, and the overall observable findings are marked as follows:

|Latest Observable Finding|Overall Observable Finding|
|-------------------------|--------------------------|
|Malicious|If one of the integration vendors reports the observable as Malicious, then the overall observable finding is marked as Malicious.|
|Suspicious|If none of the integration vendors report the observable as Malicious, one of them reports it as Suspicious, and then the overall observable finding is marked as Suspicious.|
|Clean|If all the integration vendors report the observable as Clean, then the overall observable finding is marked as Clean.|
|Unknown|If none of the integration vendors report the observable as Malicious or Suspicious and one of them report it as Unknown, then the overall observable finding is marked as Unknown.|

## Observable finding override modes

You can control how threat lookup results update observable findings by configuring the override mode. Navigate to **Threat Intelligence** &gt; **Administration** &gt; **Properties** and set the **Observable finding override mode** property to one of the following values:

-   **Default** — The system always recalculates findings from threat lookup results. Any previous finding value is overwritten.
-   **Override** — Users can manually override the observable finding for a limited time. The system does not change the finding during the configured validity period.
-   **Precedence** — Findings follow a defined priority order. Severity upgrades from threat lookup results are applied immediately, while downgrades are deferred until the per-observable-type expiry window elapses. The **Precedence expiry** field on each observable type record defines how many days a higher-severity finding is retained before the system applies a downgrade. The default value is 0 days.

When using precedence mode, configure the **Observable finding precedence order** property to define the priority ranking. The default order is Malicious, Suspicious, Unknown, Clean, where Malicious has the highest priority.

