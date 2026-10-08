---
title: Metadata enrichment with ServiceNow Otto setup
description: Before running AI enrichment jobs, activate the enrichment launcher and configure data steward role access.Add the DCGEnrichLauncher script include to the Global application scope to activate the enrichment review experience.Configure the bulk\_enrich.default\_dashboard\_sys\_id system property to allow users with the data steward role to open the enrichment workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/set-up-ai-enrichment-workspace-dc.html
release: australia
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 2
keywords: [AI metadata enrichment, metadata enrichment, DCGEnrichLauncher, Data Catalog, data steward, AI metadata enrichment, enrichment workspace, DCGEnrichLauncher, Data Catalog, AI metadata enrichment, enrichment workspace, bulk\_enrich.default\_dashboard\_sys\_id, Data Catalog, data steward]
breadcrumb: [Metadata enrichment with ServiceNow Otto, Data Catalog, Workflow Data Fabric]
---

# Metadata enrichment with ServiceNow Otto setup

Before running AI enrichment jobs, activate the enrichment launcher and configure data steward role access.

To use Metadata enrichment with ServiceNow Otto, complete the following setup tasks:

-   [Activate the enrichment launcher](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/set-up-ai-enrichment-workspace-dc.md): Add the **DCGEnrichLauncher** script include to the Global application scope to activate the enrichment review experience.
-   [Grant data steward access to the enrichment workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/set-up-ai-enrichment-workspace-dc.md): Configure the **bulk\_enrich.default\_dashboard\_sys\_id** system property so that users with the data steward role can open the enrichment workspace.

For system properties that control enrichment batch size, parallel lanes, and lane timeouts, see [Data assets enrichment system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/ai-enrichment-system-properties-dc.md) These properties are optional. The default values work for most implementations. Adjust them only if enrichment jobs are running slower than expected or you are tuning performance.

## Activate the enrichment launcher

Add the **DCGEnrichLauncher** script include to the Global application scope to activate the enrichment review experience.

### Before you begin

The following applications must be installed:

-   Otto for Workflow Data Fabric \(sn\_nowassist\_wdf\) version 2.1.4 or later

Role required: admin

### About this task

The **DCGEnrichLauncher** script include activates the enrichment review experience.

### Procedure

1.  Set the **Application scope** to **Global**.

2.  Navigate to **All** &gt; **Script Includes**.

3.  Filter the list by **Scope** = `ServiceNow Data Catalog`, then open **DCGEnrichLauncher**.

4.  Select **Insert and Stay** to add **DCGEnrichLauncher** to Global application scope.

    The newly inserted script is in the Global application scope.


## Grant data steward access to the enrichment workspace

Configure the **bulk\_enrich.default\_dashboard\_sys\_id** system property to allow users with the data steward role to open the enrichment workspace.

### Before you begin

Role required: admin

### About this task

The **bulk\_enrich.default\_dashboard\_sys\_id** system property controls who can open the enrichment workspace that monitor-progress links lead to.

### Procedure

1.  Navigate to **All** &gt; **System Properties**.

2.  Filter the list by **Scope** = `ServiceNow Data Catalog`, then open the **bulk\_enrich.default\_dashboard\_sys\_id** property record.

3.  In the **Read roles** field, add `df_data_steward`.

4.  Save the property record.


### Result

Users with the df\_data\_steward role can open the enrichment workspace from monitor-progress links and the job-completion email.

