---
title: Activate Change Management - Risk Assessment
description: You can activate the Change Management - Risk Assessment plugin \(com.snc.change\_management.risk\_assessment\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/activate-change-risk-assessment.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Change Management plugins, Configure, Change Management, IT Service Management]
---

# Activate Change Management - Risk Assessment

You can activate the Change Management - Risk Assessment plugin \(com.snc.change\_management.risk\_assessment\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Change Management - Risk Assessment activates these related plugins if they are not already active.

<table id="table_rvr_yk2_3w"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment Components\[com.snc.assessment\]

</td><td>

Provides the core components required for legacy surveys.

</td></tr><tr><td>

Best Practice - Change Risk Calculator\[com.snc.bestpractice.change\_risk\]

</td><td>

Provides simple risk and impact calculations for change management.

</td></tr><tr><td>

Assessment Designer\[com.glide.assessment\_designer\]

</td><td>

Provides an interface to create and edit the Change Risk Assessment form that is required to collect user information on risk of the change request.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).


## What to do next

You can [define risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_DefineARiskAssessment.md) conditions for change requests.

**Parent Topic:**[Change Management plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/change-plugins.md)

**Related topics**  


[Request ITSM Roles- Change Management]()

[Activate Business Stakeholder]()

[Activate Change Management - State Model]()

[Activate Change Management - Collision Detector]()

[Activate Best Practice - Change Risk Calculator]()

[Activate Change Management - Change Schedule]()

[Activate Change Management - Standard Change Catalog]()

[Activate Change Management - Change Success Score]()

[Activate Change Management - Mass Update CI]()

[Activate Change Management -Approval policy]()

[Activate Change Management - CAB Workbench]()

[Activate Change Management ATF Tests]()

[Activate Change Management - Core]()

[Request Change Management - Risk Assessment]()

[Request Change Management - Standard Change Template Intelligence]()

[Change Management - Predictive Intelligence Core]()

[Activate Change Management - Change Flows]()

[Activate Change Management - Change Velocity dashboard]()

[Activate Change Management - Change Models]()

[Activate Change Management Success Probability]()

[Activate Change Management - Data Archiving]()

[Risk conditions and calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/change-risk-assess-detect-conflict.md)

[Change Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/r_ChangeManagementProperties.md)

[List of Australia plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

