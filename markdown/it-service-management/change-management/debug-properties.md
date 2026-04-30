---
title: Change Management troubleshooting properties
description: Use the Change Management troubleshooting properties and change the value of the properties to get additional logging details for the feature.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy: Change Management Platform Analytics Solutions, Using Change Management, Change Management, IT Service Management]
---

# Change Management troubleshooting properties

Use the Change Management troubleshooting properties and change the value of the properties to get additional logging details for the feature.

The following properties are available for further configuration. To list them, enter `sys_properties.list` in the navigator text box.

<table id="table_ax1_nvt_yr"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

change.conflict.log

</td><td>

The logging property that controls logging level displayed for Change Management while detecting the change conflicts.-   Type: choice list
-   Default value: notice

</td></tr><tr><td>

com.snc.change\_management.cab.log

</td><td>

The logging property that controls the logging level displayed for Change Management when using the CAB functionality.-   Type: choice list
-   Default value: info

</td></tr><tr><td>

com.snc.change\_management.core.log

</td><td>

The logging property that controls level logging displayed for Change Management .-   Type: choice list
-   Default value: warn

</td></tr><tr><td>

com.snc.change\_management.policy.approval.log

</td><td>

The debug logging property that provides the detailed logging information of the workflow activity when using Change Approval Policies.Type: choice list

</td></tr></tbody>
</table>**Parent Topic:**[Legacy: Change Management Platform Analytics Solutions](../../../use/dashboards/application-content-packs/change-content-pack.md)

