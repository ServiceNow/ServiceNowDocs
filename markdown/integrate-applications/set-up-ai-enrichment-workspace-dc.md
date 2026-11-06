---
title: Metadata enrichment with ServiceNow Otto setup
description: Before running AI enrichment jobs, activate the enrichment launcher and configure data steward role access.Add the DCGEnrichLauncher script include to the Global application scope to activate the enrichment review experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/set-up-ai-enrichment-workspace-dc.html
release: australia
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 1
keywords: [AI metadata enrichment, metadata enrichment, DCGEnrichLauncher, Data Catalog, data steward, AI metadata enrichment, enrichment workspace, DCGEnrichLauncher, Data Catalog]
breadcrumb: [Metadata enrichment with ServiceNow Otto, Data Catalog, Workflow Data Fabric]
---

# Metadata enrichment with ServiceNow Otto setup

Before running AI enrichment jobs, activate the enrichment launcher and configure data steward role access.

To use Metadata enrichment with ServiceNow Otto, add the **DCGEnrichLauncher** script include to the Global application scope to activate the enrichment review experience. For details, see [Activate the enrichment launcher](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/set-up-ai-enrichment-workspace-dc.md).

For system properties that control enrichment batch size, parallel lanes, and lane timeouts, see [Data assets enrichment system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/ai-enrichment-system-properties-dc.md). These properties are optional. The default values work for most implementations. Adjust them only if enrichment jobs are running slower than expected or you are tuning performance.

## Activate the enrichment launcher

Add the **DCGEnrichLauncher** script include to the Global application scope to activate the enrichment review experience.

### Before you begin

The following applications must be installed:

-   Otto for Workflow Data Fabric \(sn\_nowassist\_wdf\) version 2.1.4 or later

Role required: admin

### About this task

The **DCGEnrichLauncher** script include activates the enrichment review experience.

### Procedure

1.  In the Unified Navigation menu, select the picker icon \(\[Omitted image "icon-scope.png"\] Alt text:\), then set the **Application scope** to **Global**.

    \[Omitted image "dc-bulk-enrich-select-scope.png"\] Alt text: Application scope picker set to Global.

2.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

3.  Filter the list by **Application** = `ServiceNow Data Catalog`, then open **DCGEnrichLauncher**.

    \[Omitted image "dc-bulk-enrich-find-script.png"\] Alt text: Script Includes list filtered by ServiceNow Data Catalog application, showing DCGEnrichLauncher.

4.  Right-click the form header and select **Insert and Stay** to add **DCGEnrichLauncher** to Global application scope.

    \[Omitted image "dc-bulk-enrich-add-script.png"\] Alt text: DCGEnrichLauncher script include added to the Global application scope.

    The newly inserted script is in the Global application scope.

    \[Omitted image "dc-bulk-enrich-script-added.png"\] Alt text: DCGEnrichLauncher script include confirmed in the Global application scope.


