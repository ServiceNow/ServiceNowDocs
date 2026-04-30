---
title: Amazon Web Services \(AWS\) Security Hub integration
description: AWS Security Hub is a cloud security posture management \(CSPM\) service that provides automated and continuous security checks and best practice checks against your AWS resources.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Amazon Web Services \(AWS\) Security Hub integration

AWS Security Hub is a cloud security posture management \(CSPM\) service that provides automated and continuous security checks and best practice checks against your AWS resources.

## Overview of the AWS Security Hub integration

AWS Security Hub enables you to identify issues in your configurations. Security Hub aggregates your security alerts, which are referred as findings. AWS Security Hub generates these findings in a standardized format and prioritizes them so that you can more easily enrich, investigate, and remediate them. You can use the AWS Security Hub integration to ingest Security Hub findings and automatically create security incidents in Security Incident Response.

AWS Security Hub integration in SIR follows a bidirectional architecture. SIR ingests Security Hub findings data to create a security incident and simultaneously updates a Security Hub finding with any updates in the corresponding security incident.

See the following diagram to learn how AWS Security Hub integrates with the ServiceNow AI Platform Security Operations applications.

![How AWS Security Hub integrates with the ServiceNow Platform.](../image/aws-security-hub-overview.png)

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

Use the key features of this integration to do the following actions:

-   Discover AWS Security Hub findings that are candidates for security incidents and automate the creation of these security incidents.
-   Map AWS Security Hub findings and entity fields to SIR security incident fields.
-   Filter AWS Security Hub findings.
-   Aggregate findings to existing open security incidents so that you don't have to create duplicate security incidents.
-   Automate AWS Security Hub findings status updates for Security Incident Response so that you can create and close security incidents.

    **Note:** ServiceNow also updates the status of AWS Security Hub findings based on the creation, progress, or closure of the security incident. This update also includes comments of aggregated and new findings.

-   Schedule findings ingestion to create security incidents periodically.
-   Synchronize AWS Security Hub finding comments with SIR Work notes.

## Learn about this integration

|Document identifier|Document title|
|-------------------|--------------|
|AWS Security Hub product documentation website|[AWS Security Hub Documentation website](https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html)|
|ServiceNow product documentation website|[ServiceNow Product Documentation website](https://servicenow.com/docs)|

