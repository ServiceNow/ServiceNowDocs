---
title: Activate Service Portfolio Management
description: The Service Portfolio Management Core plugin \(com.snc.service\_portfolio\_core\) is available by default for ITSM licensed customers. You can activate additional available related plugins for enhanced features and functionality.
locale: en-US
release: xanadu
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Activate Service Portfolio Management

The Service Portfolio Management Core plugin \(com.snc.service\_portfolio\_core\) is available by default for ITSM licensed customers. You can activate additional available related plugins for enhanced features and functionality.

## Before you begin

Role required: admin

## About this task

The Service Portfolio Management Foundation plugin \[com.snc.service\_portfolio\] enables your organization to document portfolios, taxonomies, services, and service offerings using a standardized, structured format. It contains demo data and activates related plugins. The Foundation plugin is activated out of the box and activates related plugins, if they're not already active. For general information, see [Service Portfolio Management](../reference/SPM2-landing-page.md).

<table id="table_q5j_gny_ngb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Portfolio Management Core\[com.snc.service\_portfolio\_core\]

</td><td>

Adds the Service Offering table \[service\_offering\] to the Configuration Management Database \(CMDB\).Available by default for users with ITSM SKUs.

</td></tr><tr><td>

Service Catalog core applications\[com.glideapp.servicecatalog\]

</td><td>

Enables integrations with the Service Catalog application and its capabilities.

</td></tr><tr><td>

Report Engine- use summary table for reports\[com.glideapp.summary\_report\_engine\]

</td><td>

Adds the glide.report\_summary\_engine system property and enables the Summary Sets reporting engine for all reports within Service Portfolio Management.

</td></tr></tbody>
</table>Several additional plugins offer increased functionality to Service Portfolio Management Foundation. Activate these plugins to enhance your experience.

<table id="table_ily_qwq_g3b"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Portfolio Management SLA Commitments\[com.snc.service\_portfolio.sla\_commitment\]

</td><td>

Adds SLA Commitment support to Service Portfolio Management. Includes demo data.

</td></tr><tr><td>

Service Portfolio Management Taxonomy Content Pack\[com.snc.spm.content\]

</td><td>

Provides sample taxonomy metadata, complete with portfolio, layers, and nodes. Demo data includes services and service offerings, including related items, such as SLAs, incidents, changes, and more. Includes demo data.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configuring Service Portfolio Management](../concept/SPM2-configuring.md)

**Related topics**  


[Installed with Service Portfolio Management](../reference/r_InstalledWSPM2.md)

