---
title: Roll up MITRE-ATT&amp;CK information using MISP enrichment results
description: Roll up the MISP enrichment results manually if you haven't enabled the automatic rollup of MISP information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/rollup-mitre-information-using-misp-enrichment-results.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using MISP to investigate and analyze threats, MISP integration for Security Operations, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Roll up MITRE-ATT&amp;CK information using MISP enrichment results

Roll up the MISP enrichment results manually if you haven't enabled the automatic rollup of MISP information.

## Before you begin

Role required: sn\_si.analyst

## About this task

Use the base system auto-extraction rules to import the MITRE-ATT&amp;CK information from the MISP integration. The MISP integration for Security Operations introduces two base system MITRE-ATT&amp;CK technique extraction rules for MISP - MISP galaxies and MISP tags. For more information on auto-extraction rules in MITRE-ATT&amp;CK, see [auto-extract technique rules for importing MITRE-ATT&amp;CK information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/auto-extract-technique-rules.md).

If you have enabled [automatic rollup of MITRE-ATT&amp;CK information using MISP enrichment results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/review-the-misp-integration-settings.md) to a security incident, the information is automatically rolled up. If you have not enabled automatic rollup, you can do this task manually.

## Procedure

1.  Navigate to **All** &gt; **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to enrich with the MITRE-ATT&amp;CK information.

3.  Click **Show All Related Lists** and the **MISP Enrichment Results** tab.

4.  Select the observable and from the Actions menu, click **Roll up MITRE ATT&amp;CK Information to SI**.

    You can select multiple observables and then roll up the information.

5.  To confirm the changes, click **Reload**.

    The following example shows how to select an observable and roll up the MISP enrichment results to the security incident.

    \[Omitted image "misp-mitre-rollup.gif"\] Alt text: Roll up MITRE information to a security incident.


## Result

You can view the MITRE-ATT&amp;CK Card to confirm that the MISP Enrichment Results have been rolled up to the security incident.

**Parent Topic:**[Using MISP to investigate and analyze threats](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/using-misp-to-detect-and-analyze-threats.md)

