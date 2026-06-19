---
title: Deployment and synchronization integrations
description: The AES/AEMC and Update set integrations control how custom app deployments are governed and how scan results are synchronized across your instance stack.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/deployment-sync-integrations.html
release: australia
product: Impact
classification: impact
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Deployment and synchronization integrations

The AES/AEMC and Update set integrations control how custom app deployments are governed and how scan results are synchronized across your instance stack.

Unlike the Definitions, Exception Reason, and User Story integrations, which act on individual findings or definitions,these integrations operate at the instance level, enforcing governance across deployment pipelines and keeping scan data consistent between developer and production instances.

## AES/AEMC integration

The AES/AEMC integration intercepts custom app deployment requests submitted from App Engine Studio or ServiceNow Studio and runs a Scan EngineScan Engine compliance check before allowing the request to advance. Deployments that do not meet the configured conditions are rejected and the application author receives an email with scan details.

This integration is configured on the production controller instance only. Deployment pipelines must already be configured in ServiceNow production instances before enabling it. No OAuth credentials or My SN Instances authentication are required beyond a single My SN Instances record designating the production controller.

**Important:** The pass condition defaults to a scan score of 100 and the scan timeout defaults to 10 minutes. Both values are configurable.

## Update set integration

The Update set integration automatically synchronizes update set scan results from developer instances to all Production instances registered in My SN Instances when a scan is marked complete. Optionally, enable summary scan synchronization to keep update set summaries in sync across instances.

**Note:** The Update set integration requires the `admin` role, not the Scan Engine-specific roles used by other integrations. My SN Instances registration and authentication must be complete before configuring this integration. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md).

-   **[Configure AES/AEMC integration properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/aes-aemc-integration-properties.md)**  
Configure the AES/AEMC integration to enforce automated Scan Engine compliance checks on custom app deployment requests from App Engine Studio and ServiceNow Studio.
-   **[Configure update set integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/update-set-integration.md)**  
Configure the update set integration to automatically synchronize update set scan results from developer instances to the production instance.

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-integration-scan-engine.md)

