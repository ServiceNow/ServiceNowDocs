---
title: Components installed with Automation Discovery
description: Tables and roles are installed with activation of the Automation Discovery plugin.Create automation discovery reports, flags automation opportunities, and takes actions on them.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install Automation Discovery, Automation Discovery, Platform Analytics]
---

# Components installed with Automation Discovery

Tables and roles are installed with activation of the Automation Discovery plugin.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automation Discovery Processed Message\[sn\_auto\_discovery\_processed\_message\]

</td><td>

References to the original data source records \(ex: incidents\). Does not include duplicated records.

</td></tr><tr><td>

Automation Discovery Param\[sn\_auto\_discovery\_param\]

</td><td>

Table containing parameters for reports.

</td></tr><tr><td>

Automation Discovery Label\[sn\_auto\_discovery\_labelled\_message\]

</td><td>

References to the report records.

</td></tr><tr><td>

Automation Discovery Intent\[sn\_auto\_discovery\_intent\]

</td><td>

Table containing automation discovery reports. Referenced by the processed message and report trace.

</td></tr><tr><td>

Automation Discovery Group\[sn\_auto\_discovery\_group\]

</td><td>

Table containing the automation opportunities in a report.

</td></tr><tr><td>

Automation Discovery Message Content\[sn\_auto\_discovery\_message\_content\]

</td><td>

References to the original data source records \(ex. incidents\). Includes duplicated records.

</td></tr><tr><td>

Automation Discovery Report\[sn\_auto\_discovery\_report\]

</td><td>

Reports previously created using Automation Discovery.

</td></tr><tr><td>

Automation Discovery Job\[sn\_auto\_discovery\_job\]

</td><td>

Table that manages the execution of Automation Discovery reporting jobs.

</td></tr><tr><td>

Automation Discovery Report Trace\[sn\_auto\_discovery\_report\_trace\]

</td><td>

History of the Natural Language Understanding \(NLU\) intents added due to the report's intents or clusters.

</td></tr><tr><td>

Automation Discovery Report Definition\[sn\_auto\_discovery\_report\_definition\]

</td><td>

Table defining how a report runs and the report status. Multiple reports can run from a single report definition.

</td></tr><tr><td>

Automation Discovery Cluster\[sn\_auto\_discovery\_cluster\]

</td><td>

Uncategorized clusters of records from the report. Referenced by the processed message and report trace.

</td></tr></tbody>
</table>## Roles installed

## Discovery author \[sn\_auto\_discovery.DiscoveryAuthor\]

Create automation discovery reports, flags automation opportunities, and takes actions on them.

### Contains Roles

The Discovery author \[sn\_auto\_discovery.DiscoveryAuthor\] role contains the nlu\_user role.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

