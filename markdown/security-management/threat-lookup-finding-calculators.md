---
title: Threat Lookup Finding Calculators
description: Threat Lookup Finding Calculator helps you calculate the observable findings based on the responses received.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
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

