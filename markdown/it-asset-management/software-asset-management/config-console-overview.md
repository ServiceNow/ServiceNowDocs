---
title: Configuration Console overview
description: The Configuration Console organizes configuration items, tracks setup progress, and offers shortcuts to reduce manual effort.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/config-console-overview.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Configuration Console for Software Asset Management, Software Asset Management installation methods, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Configuration Console overview

The Configuration Console organizes configuration items, tracks setup progress, and offers shortcuts to reduce manual effort.

## Configuration Summary page

The Configuration Summary page is the landing page of the Configuration Console. The page has two main areas:

-   **Setup status**

    Displays a tile for each of the three configuration categories with the count of items configured and the total items in that category. From each tile, select **Get Started** to open the first item in that category.

-   **Configuration activity**

    Displays the configuration changes that have been recorded on this instance. Use the **Configured items** tab to review individual items that have been marked as configured. Use the **Completed batches** tab to review changes that have been grouped into completed batched update sets.


## Reuse and AI-assisted configuration

The console header offers two shortcuts and the item-by-item workflow. Package a completed configuration for reuse on another instance, or use AI to configure supported items.

-   **Package and download**

    Group completed configuration changes into a batched update set and download it. Reuse the update set to apply the same configuration on another instance without redoing the manual work.

-   **Configure with AI**

    Open ServiceNow Otto to configure supported items with AI assistance. Configure with AI is available for Content Service setup, Groups, and Users.


## Configuration Console modules

The Configuration Console modules for Software Asset Management \[[Configuration Console modules for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/config-console-overview.md)\] table lists every module that remains after installation, grouped by category. Each row includes a description, a reference link, and the roles required to access the module. To configure a module, select it in the Configuration Console, or enter its name in **Search configurations** to find it. Configure the settings, and select **Mark as configured** to update the setup progress on the Configuration Summary page.

<table id="config-items"><thead><tr><th>

Category

</th><th>

Configuration items

</th><th>

Description

</th><th>

Roles required

</th><th>

Reference

</th></tr></thead><tbody><tr><td rowspan="6">

Software foundations

</td><td>

Override customizations

</td><td>

Resolve conflicts between customizations and the default components of Software Asset Management to keep forms, scripts, UI policies, and business rules upgrade-ready.

</td><td>

admin

</td><td>

See [Revert Software Asset Management customizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/revert-sam-customizations.md).

</td></tr><tr><td>

Content job progress

</td><td>

Track the first-time run of the content jobs that load the software content library data supporting Software Asset Management features.

</td><td>

cds\_client\_admin

</td><td>

See [Monitoring content job progress](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/content-job-progress.md).

</td></tr><tr><td>

Content Service setup

</td><td>

Opt in to the Software Asset Management Content Service to share unnormalized software installation data from your organization with ServiceNow® to improve the normalization process.

</td><td>

-   sam\_admin
-   sn\_ia\_config.ia\_user

</td><td>

See [Configure Content Service setup using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-content-service-otto.md).

</td></tr><tr><td>

Properties

</td><td>

Configure the properties that influence how reconciliation, software models, normalization, and publisher-specific rules run. The console groups these properties under Reconciliation, Software model, Normalization, Publisher, and Other.

</td><td rowspan="2">

admin

</td><td>

See [Software Asset Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sam-properties.md).

</td></tr><tr><td>

Otto skills

</td><td>

Enable and customize the preconfigured AI skills that automate the Software Asset Management workflows.**Note:** This module appears only when ServiceNow Otto for Software Asset Management \(SAM\) is installed.

</td><td>

See [Generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/explore-generative-ai-skills-now-assist-sam.md).

</td></tr><tr><td>

Migrate software installations

</td><td>

Migrate CMDB software installations to the Software Asset Management Software installations \[samp\_m2m\_candidate\_install\] table.

</td><td>

-   sam\_admin
-   sn\_ia\_config.ia\_user

</td><td>

See [Migrate software installations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/t_MigrateSWInstalls.md).

</td></tr><tr><td rowspan="3">

Governance

</td><td>

Scheduled jobs

</td><td>

View, create, and export the scheduled jobs that automate recurring Software Asset Management processes such as normalization and reconciliation.

</td><td>

system\_scheduler\_admin

</td><td>

See [Configure scheduled jobs in the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/manage-scheduled-jobs-sam-using-config-console.md).

</td></tr><tr><td>

Groups

</td><td>

Create groups and assign users and roles that manage Software Asset Management operations and notifications.

</td><td rowspan="2">

admin

</td><td rowspan="2">

See [Configure groups and users using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-sam-team-using-ai.md).

</td></tr><tr><td>

Users

</td><td>

Import users and assign roles that establish access and capabilities across Software Asset Management.

</td></tr><tr><td rowspan="2">

Data management

</td><td>

SSO

</td><td>

Configure the SSO integration for Software Asset Management.

</td><td rowspan="2">

-   sam\_admin
-   sn\_ia\_config.ia\_user

</td><td>

See [SSO integration in Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sam-sso-integration-config-console.md).

</td></tr><tr><td>

Direct connection

</td><td>

Configure the direct connection integration for Software Asset Management.

</td><td>

See [Direct connection integration in Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sam-direct-connection-config-console.md).

</td></tr></tbody>
</table>**Parent Topic:**[Configuration Console for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/config-console-sam.md)

**Related topics**  


[Configuration Console for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/config-console-sam.md)

