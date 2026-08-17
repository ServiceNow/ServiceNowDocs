---
title: Configure the Early Warning for Security Exposure Management integration
description: Install and configure the Early Warning for Security Exposure Management integration plugin to ingest vulnerability intelligence and enrich your vulnerability database with threat signals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/t-configure\_early\_warning\_integration.html
release: yokohama
topic_type: task
last_updated: "2026-06-23"
reading_time_minutes: 2
keywords: [configure, Early Warning, integration setup, Vulnerability Response]
breadcrumb: [Early Warning for Security Exposure Management, Integrate, Unified Security Exposure Management, Security Operations]
---

# Configure the Early Warning for Security Exposure Management integration

Install and configure the Early Warning for Security Exposure Management integration plugin to ingest vulnerability intelligence and enrich your vulnerability database with threat signals.

## Before you begin

Before you begin:

-   Verify that Unified Security Exposure Management \(Vulnerability Response v30.x\) is installed and configured in your instance.
-   Verify that the Vulnerability Integration Framework plugin is activated.
-   Obtain Armis Early Warning feed credentials and verify access to the threat intelligence API.

Role required: sn\_sec\_cvd.read: Viewing Early Warning for Security Exposure Management health/CVD records.

**Note:** Write access to sn\_vul\_ew\_cvd\_attributes table is not exposed to any user role; the integration manages these attributes internally.

## About this task

By configuring the Early Warning for Security Exposure Management integration, you enable your vulnerability management system to access vulnerability intelligence, allowing your security team to prioritize and respond to high-risk vulnerabilities.

## Procedure

1.  Navigate to **All** and enter sn\_sec\_int\_integration.LIST in the Filter Navigator.

2.  In the **Third-party Integrations** list, select **Early Warning for Security Exposure Management**.

3.  Select **Integration Instances** tab.

4.  Configure the integration parameters in the **Integration Instance Parameters** related tab.

    1.  Select **armis\_api\_url** and enter the Armis API endpoint URL in the **Value** field.

    2.  Select **armis\_api\_key** and enter the Armis authentication credentials in the **Password value** field.

5.  Verify that delta \(incremental\) ingestion is enabled.

    Delta ingestion processes only new or changed threat records, minimizing API calls and avoiding re-enrichment of unchanged records between runs.

6.  Select **Save and Activate** to enable the integration.

    The integration is now active and the framework will begin delta synchronization on the next scheduled run.

7.  Verify that the early warning flag \(`ew_exists`\) is visible in your CVDB list view and form pages.

    The list view column displays the enriched threat signal status for each CVE record. When you select a row, the CVE form opens.


## Result

Your Early Warning for Security Exposure Management integration is now configured and active. The integration will:

-   Ingest threat signals on a scheduled cadence.
-   Enrich matching CVDB records with vulnerability intelligence attributes. See Libraries in the List view table in [Security Exposure Management Workspace List view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/sem-workspace-list-page.md) for more information.
-   Propagate early warning status to related vulnerability records.
-   Update risk scores to reflect early warning signals.

## What to do next

After configuring the integration, consider the following next steps:

-   Configure risk rules to weight the early warning flag in your vulnerability risk calculation
-   Create custom Vulnerability Crisis Management \(VCM\) workflows to trigger on early warning CVEs.
-   Review and customize the Early Warning dashboard to fit your team's reporting needs.

