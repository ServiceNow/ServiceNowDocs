---
title: Synchronize Docusign with ServiceNow
description: Synchronize ServiceNow with Docusign to access Docusign accounts, templates, and envelopes from the Docusign spoke.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Docusign eSignature Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Synchronize Docusign with ServiceNow

Synchronize ServiceNow with Docusign to access Docusign accounts, templates, and envelopes from the Docusign spoke.

## Before you begin

Role required: admin

-   Request IntegrationHub subscription
-   Activate Docusign spoke
-   [Set up Docusign eSignature spoke using JWT grant](setup-docusign-jwt.md#)

## About this task

Schedule a job to synchronize Docusign with your ServiceNow instance daily, or synchronize data as needed.

## Procedure

1.  Schedule a job to synchronize Docusign data with your ServiceNow instance.

    1.  Navigate to **Docusign** &gt; **Scheduled Job**.

        The Get Accounts &amp; Templates scheduled job opens.

    2.  Select **Active**.

    The Docusign eSignature spoke synchronizes accounts, templates, and envelopes daily.

2.  Synchronize Docusign data as needed with a UI action.

    1.  Navigate to **Docusign** &gt; **Accounts**.

        The Accounts \[sn\_docusign\_spoke\_accounts\] table opens.

    2.  Click the **Get Accounts** related link.

    The system synchronizes all accounts linked through an OAuth Credential record and populates the Templates and Envelopes tables with Docusign data. Use template and envelope records when constructing flows.


