---
title: Understanding the Vulnerability Response Integration with Palo Alto Prisma Cloud
description: Prisma Cloud is an API-based cloud infrastructure security solution. It connects to your cloud environment and monitors the resources deployed on the public cloud environments, such as Amazon Web Services \(AWS\), Microsoft Azure, and so on. You get complete visibility and control over risks within your public cloud infrastructure.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuration Compliance integrations, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Understanding the Vulnerability Response Integration with Palo Alto Prisma Cloud

Prisma Cloud is an API-based cloud infrastructure security solution. It connects to your cloud environment and monitors the resources deployed on the public cloud environments, such as Amazon Web Services \(AWS\), Microsoft Azure, and so on. You get complete visibility and control over risks within your public cloud infrastructure.

The Vulnerability Response Integration with Palo Alto Prisma Cloud application facilitates ingestion of policies and alerts from Prisma Cloud, as tests and test results respectively, in the Configuration Compliance application. With the right configuration, the test results can be managed seamlessly by assigning appropriate risk scores, and grouping and assigning them to relevant users and groups.

## Available versions

The table lists the applications that Vulnerability Response Integration with Palo Alto Prisma Cloud depends on, along with the version of the application.

|Application|Version|
|-----------|-------|
|Prisma Cloud integration for Security Operations|2.3|
|Configuration Compliance|14.7|
|Security Support Common|13.5|
|Vulnerability Response|18.0|

## ServiceNow Prisma Cloud Integrations

The Vulnerability Response Integration with Palo Alto Prisma Cloud application helps import the Prisma data to your ServiceNow instance to enrich your instance for better management. A series of scheduled jobs invoke the integrations automatically. You can also run these scheduled jobs manually. Scheduled jobs simplify the test results remediation life cycle by keeping the instance updated by retrieving data periodically from Prisma Cloud.

Prisma Cloud integration tasks involve the following roles.

-   sn\_vul\_prismacloud.configure\_integration: Ability to read, write, and delete records.
-   sn\_vul\_prismacloud.read\_integration: Ability to read records.

## Viewing the integrations

You can view the integrations that are part of the Vulnerability Response Integration with Palo Alto Prisma Cloud by navigating to **Prisma Cloud Integration** &gt; **Integrations**.

The following integrations are available in the base system.

<table id="table_sbn_qtp_dt"><thead><tr><th>

Run Sequence

</th><th>

Schedule

</th><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Weekly

</td><td>

Prisma Policy Integration

</td><td>

-   Retrieves policies from Prisma Cloud and creates test entries in your instance.
-   It does not provide incremental support. If you run the integration for the last 10 days, it shows the result for previous integration runs as well.

</td></tr><tr><td>

2

</td><td>

Daily

</td><td>

Prisma Alerts Integration

</td><td>

-   Retrieves alerts from Prisma Cloud and creates test results entries in your instance.
-   Provides incremental support. The integration runs daily after the last integration run time.

</td></tr></tbody>
</table>-   **[Preparing for installing the Vulnerability Response Integration with Palo Alto Prisma Cloud](preparing-prisma-cloud.md)**  
Prepare for installing the Vulnerability Response Integration with Palo Alto Prisma Cloud by performing setup tasks.
-   **[Install and configure the Vulnerability Response Integration with Palo Alto Prisma Cloud application](install-and-configure-prisma-cloud.md)**  
Install the Vulnerability Response Integration with Palo Alto Prisma Cloud application to use the imported data from Prisma Cloud. Use this data to prioritize and remediate misconfigurations on your assets.
-   **[Configure the Vulnerability Response Integration with Palo Alto Prisma Cloud application](configure-vulnerability-response-prisma-cloud.md)**  
Configure the Vulnerability Response Integration with Palo Alto Prisma Cloud application. Use the imported data from Prisma Cloud to prioritize and remediate misconfigurations on your assets.
-   **[Verify the Vulnerability Response Integration with Palo Alto Prisma Cloud import run status](verify-integration-run.md)**  
Use the Vulnerability Response Integration with Palo Alto Prisma Cloud import run status to verify the success of your integration runs and to identify any issues.
-   **[Data mapping](cc-prisma-import-data.md)**  
The data from Prisma Cloud is imported in the Configuration Compliance module of the ServiceNow instance.
-   **[Prisma Cloud REST Messages](prisma-cloud-rest-messages.md)**  
Prisma REST messages are used to make calls to the Prisma Application Programming Interface \(API\) to fetch the compliance data.

**Parent Topic:**[Configuration Compliance integrations](../../../vulnerability-config-compliance/concept/vuln-config-compl-integrations.md)

