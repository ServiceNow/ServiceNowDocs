---
title: Deployment and synchronization integrations
description: The AES/AEMC and Update set integrations control how custom app deployments are governed and how scan results are synchronized across your instance stack.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/deployment-sync-integrations.html
release: australia
topic_type: concept
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [Scan Engine integrations, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Deployment and synchronization integrations

The AES/AEMC and Update set integrations control how custom app deployments are governed and how scan results are synchronized across your instance stack.

Unlike the Definitions, Exception Reason, and User Story integrations, which act on individual findings or definitions, these integrations operate at the instance level, enforcing governance across deployment pipelines and keeping scan data consistent between developer and production instances.

## AES/AEMC integration

The AES/AEMC integration intercepts custom app deployment requests submitted from App Engine Studio or ServiceNow Studio and runs a Scan Engine compliance check before allowing the request to advance. Deployments that do not meet the configured conditions are rejected and the application author receives an email with scan details.

Enable AES/AEMC on the production instance only. Create one My SN Instances record with the `environment` set to Production and an instance name that matches the `instance_name` system property. The record does not need to be validated, and it does not designate the controller. It unlocks the **Enable AES/AEMC Integration \(Production Instance Only\)** option in Scan Engine Properties and maps Scan Engine to your production controller, so Deployment Pipelines can use the Scan Engine flow for approvals and deployments. On non-production instances, the option is read-only and set to false.

Configure the controller on the Environment record in Pipelines and Deployments, by selecting the **Is Controller?** checkbox. Deployment pipelines must already be configured in ServiceNow production instances before you enable AES/AEMC.

Cross-instance deployment calls also depend on the `sn_pipeline_environment` table from Pipelines and Deployments. Each Environment record has an **Instance credential** field that points to a Connection and Credential Alias.

**Important:** The pass condition defaults to a scan score of 100 and the scan timeout defaults to 10 minutes. Both values are configurable.

## Update set integration

The Update set integration sends update set scan results to Production and to all other instances in the integration, so you can check results from any instance. Enable it on each instance whose scan data you want to share by selecting **Enable update set summary scan synchronization** on the **Update Set Scanning** tab of Scan Engine Properties.

**Note:** The scanning user needs the `sn_se.scan_engine_user` role, or `sn_se.scan_engine_admin` if that user also manages definitions. The account that receives the summary sync needs `sn_se.internal_rest_integration`. The `admin` role isn't required. My SN Instances registration and authentication must be complete before configuring this integration. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md).

-   **[Configure AES/AEMC integration properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/aes-aemc-integration-properties.md)**  
Configure the AES/AEMC integration to enforce automated Scan Engine compliance checks on custom app deployment requests from App Engine Studio and ServiceNow Studio.
-   **[Configure update set integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/update-set-integration.md)**  
Synchronize update set scan results from the instance where you run the scan to production and the other instances in the integration.

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integration-scan-engine.md)

