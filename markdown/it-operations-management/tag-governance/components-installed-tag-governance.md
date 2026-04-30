---
title: Components installed with Tag Governance
description: Several key components are installed with, or linked to, the Tag Governance plugin to help standardize and manage your organization's tags.
locale: en-US
release: yokohama
product: Tag Governance
classification: tag-governance
topic_type: reference
last_updated: "2025-06-25"
reading_time_minutes: 2
breadcrumb: [Tag Governance reference, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Components installed with Tag Governance

Several key components are installed with, or linked to, the Tag Governance plugin to help standardize and manage your organization's tags.

## Roles installed

<table id="table_b5p_xqd_5fc"><thead><tr><th>

Role title

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

\[tag\_governance\_admin\]

</td><td>

Sets up and manages the tag governance application. Defines and enforces tag policies, manages tag categories and values, and promotes compliance with organizational standards. Performs advanced configuration and customization of tag governance features. Assign this role to application administrators.

</td><td>

-   \[itil\]
-   \[certification\_admin\]
-   \[discovery\_admin\]
-   \[flow\_operator\]

</td></tr><tr><td>

\[tag\_reports\_viewer\]

</td><td>

Views and analyzes tag reports related to tag usage and compliance. Assign this role to users who monitor and analyze tag data.

</td><td>

\[cmdb\_read\]

</td></tr></tbody>
</table>## Tag categories installed

Starting with version 1.7.0, the predefined categories listed in the table are installed with Tag Governance and require the installation of at least Service Mapping Plus version 1.16.3. For more information see [Install Service Mapping Plus](../../service-mapping/task/install-service-mapping-plus.md).

<table id="table_odc_mry_tfc"><thead><tr><th>

Tag category

</th><th>

Definition \(Regex\)

</th></tr></thead><tbody><tr><td>

Application ID

</td><td>

applicationid\|application-id\|app-id\|appid\|application id\|app id

</td></tr><tr><td>

Assignment Group

</td><td>

assignment-group\|assignment\_group\|assignment group\|assignmentgroup\|assign group

</td></tr><tr><td>

Cost Center

</td><td>

costcenter\|cost-center\|cost\_centre\|costcentre\|cost-centre\|cost centre

</td></tr><tr><td>

Environment

</td><td>

env\|envt\|environ\|environment

</td></tr><tr><td>

Owner

</td><td>

own\|owner\|owners\|ownership\|owned

</td></tr></tbody>
</table>## Properties installed

<table id="table_uxs_5yy_tfc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_itom\_tag.glide.script.block.client.globals

</td><td>

Controls the access client-side scripts have to global variables for enhanced security. If set to true, these scripts can't access global variables.-   **Type:** boolean
-   **Value:** true/false
-   **Default value:** False

</td></tr><tr><td>

sn\_itom\_tag.allow\_new\_cert\_follow\_on\_task

</td><td>

Enables the creation of new certification follow-up tasks for each audit in Tag Governance.-   **Type:** boolean
-   **Value:** true/false
-   **Default value:** False

</td></tr><tr><td>

sn\_itom\_tag.azure\_window\_size\_in\_mins

</td><td>

Time window size, in minutes, to check for changes in Azure Resources. This value helps determine the start and end times for the check:**Start time:** The time the event occurred minus the time window size.

**End time:** The time when the event occurred plus the time window size.

-   **Type:** integer
-   **Default value:** 10

</td></tr><tr><td>

sn\_itom\_tag.performance.config.bulksize

</td><td>

Sets the number of app data items to process at one time.-   **Type:** integer
-   **Default value:** 5000

</td></tr><tr><td>

sn\_itom\_tag.last\_event\_processed

</td><td>

Indicates the last tag event successfully processed to verify that the system is up to date with the latest changes.-   **Type:**string
-   **Default value:**

</td></tr><tr><td>

sn\_itom\_tag.max\_audit\_lag\_ratio

</td><td>

Sets the maximum acceptable ratio of delay for tag audits to confirm that tag policy audits are performed within a specified time frame.-   **Type:** integer
-   **Default value:** 2

</td></tr><tr><td>

sn\_itom\_tag.tag\_event\_batch\_size

</td><td>

Sets the number of tag events, such as the creation, update, or deletion of tags, processed together in a single batch.-   **Type:** integer
-   **Default value:** 500

</td></tr><tr><td>

sn\_itom\_tag.policy\_batch\_size

</td><td>

Sets the number of items processed together in a single batch when a tag policy audit is run.-   **Type:** integer
-   **Default value:** 1000

</td></tr></tbody>
</table>**Parent Topic:**[Tag Governance reference](../concept/reference-tag-governance.md)

