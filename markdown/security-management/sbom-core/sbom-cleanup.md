---
title: SBOM cleanup
description: SBOM cleanup removes older software bill of materials records that match conditions you define and can help you reduce your data volume in the SBOM Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/sbom-core/sbom-cleanup.html
release: zurich
product: SBOM Core
classification: sbom-core
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [SBOM, cleanup, purge, Security Exposure Management]
breadcrumb: [Uploading and viewing your SBOM files in the SBOM Workspace, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# SBOM cleanup

SBOM cleanup removes older software bill of materials records that match conditions you define and can help you reduce your data volume in the SBOM Workspace.

## SBOM cleanup overview

Software bill of materials \(SBOM\) data accumulates over time as ingestion jobs bring in new records. Because cleanup and ingestion act on the same underlying records, running them concurrently might produce inconsistent or partially processed data. To prevent this conflict, the system coordinates cleanup and ingestion so that only one of the two processes runs at any given time.

SBOM cleanup lets you create a one-time rule to purge older software bill of materials records that match specified conditions that you create. Cleanup runs are permanent and can't be reversed, so review your conditions carefully before running one.

## Key benefits

SBOM cleanup provides the following benefits:

-   Automates removal of outdated SBOM data
-   Provides visibility into cleanup progress with status tracking
-   Lets you define conditions that target only the records you intend to purge, rather than removing all historical data. You can set conditions such as record age and identify any product models and business applications you want to exclude from the cleanup job.

## How it works

-   Purge execution is permanent. Records removed by a cleanup run can't be retrieved or restored.
-   Cleanup and data import jobs can't run at the same time. Pause any SBOM upload and data imports before you run a cleanup job.
-   A cleanup rule is a one-time purge action. After you create it and run it, the rule does not run again on a recurring basis.
-   A failed cleanup rule is marked with a status of "Failed" along with an error message.
-   If there are no cleanup jobs in an instance, configure the first one from the SBOM cleanup configuration page. Navigate to **SBOM Workspace** &gt; **Configuration** &gt; **SBOM cleanup**.

.

