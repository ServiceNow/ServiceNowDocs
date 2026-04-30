---
title: Digital Product Release properties
description: Configure the system properties to customize various features of Digital Product Release according to your organization's needs.
locale: en-US
release: xanadu
product: Digital Product Release
classification: digital-product-release
topic_type: reference
last_updated: "2025-04-25"
reading_time_minutes: 4
breadcrumb: [Digital Product Release reference, Digital Product Release, IT Service Management]
---

# Digital Product Release properties

Configure the system properties to customize various features of Digital Product Release according to your organization's needs.

These properties are available for Digital Product Release.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_cfk_tl1_jzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_dpr.auto\_transition\_release\_to\_completed

</td><td>

Determines whether a release can be automatically moved from the Review state to Completed state when its review is finished.-   Type: true\|false
-   Default value: false
-   Other possible values: true

</td></tr><tr><td>

sn\_dpr.auto\_transition\_release\_to\_review

</td><td>

Determines whether a release can be automatically moved from the In Progress state to Review state when all its phases are completed.-   Type: true\|false
-   Default value: true
-   Other possible values: false

</td></tr><tr><td>

sn\_dpr.complete\_phase\_override

</td><td>

Enables users with specific roles to complete a release phase. The default role, sn\_dpr\_model.release\_admin, is set in the **Value** field. You can append additional roles that have write access to the release phase state, separated by commas.-   Type: string
-   Default value: sn\_dpr\_model.release\_admin
-   Other possible values: Roles that have write access to the release phase state.

</td></tr><tr><td>

sn\_dpr.max\_template\_duration

</td><td>

Specifies the maximum number of days for the duration of a release template. It is the total duration of all phases included in the template.-   Type: Integer
-   Default value: 730 days
-   Other possible values: An integer value

</td></tr><tr><td>

sn\_dpr.multi\_product.create\_independent\_releases

</td><td>

Determines whether to create individual releases that can be managed independently for each product selected during release creation.

-   When set to false, a main release is created for the primary product or service that includes individual releases for each product as dependent releases.
-   When set to true, a release bundle is created that includes independent releases for each included product.

For more information, see [Create a release with a wizard](../task/dpr-create-release-guided.md).

 -   Type: true\|false
-   Default value: false
-   Other possible values: false

</td></tr><tr><td>

sn\_dpr.multi\_product.included\_products\_limit

</td><td>

Specifies the maximum number of products that can be added as Included products when creating a multi-product release. For more information, see [Create a release with a wizard](../task/dpr-create-release-guided.md).

**Note:** This property is applicable only if sn\_dpr.multi\_product.create\_independent\_releases is set to true.

 -   Type: Integer
-   Default value: 10
-   Other possible values: An integer value

</td></tr><tr><td>

sn\_dpr.out\_of\_band\_release\_allowed

</td><td>

Determines whether a release can be created on any given date, without a release target.-   Type: true\|false
-   Default value: true
-   Other possible values: false

</td></tr><tr><td>

sn\_dpr.out\_of\_band\_release\_roles

</td><td>

Specifies the comma-separated list of roles that can create a one-off release.-   Type: string
-   Default value: sn\_dpr\_model.release\_admin

</td></tr><tr><td>

sn\_dpr.release\_calendar\_exclusions

</td><td>

Restricts the schedules shown as part of release calendar using the encoded query.

 You can use an encoded query on the cmn\_schedule table to filter and show specific schedules in the **Exclusion schedules** field on the [Release calendar](../task/dpr-create-release-calendar.md) dialog box. Blackout and Maintenance schedules are included by default.

 -   Type: string
-   Default value: sn\_dpr\_model.release\_admin

</td></tr><tr><td>

sn\_dpr.release\_kanban\_lanes

</td><td>

Shows the lanes on Kanban board in the Release execution page.-   Type: string
-   Default value: 1,2,3

</td></tr><tr><td>

sn\_dpr.sequential\_task\_execution

</td><td>

Determines whether tasks in a phase of a release are processed one after the other.When this property is set to true, tasks are processed in sequential order. At the start of a phase, the task with the lowest order in it is set to the Open state. After this task is completed, the next task in the order is opened. This process continues for the remaining tasks in the phase. If the task is an approval task, the state is moved to the Requested state.

When this property is set to false, tasks are not processed in sequential order. Instead, all its tasks are set to the Open state at the start of the phase.

-   Type: true\|false
-   Default value: true
-   Other possible values: false

</td></tr><tr><td>

sn\_dpr.stage\_workflow\_auto\_transition

</td><td>

Determines whether a stage-oriented release and its phases can automatically transition between states through the scheduled job.If this property is set to false, the phases of the release will not transition between states, even if they comply with mapped policies.

-   Type: true\|false
-   Default value: true
-   Other possible values: false

</td></tr><tr><td>

sn\_dpr.VulnerabilitiesTypeMapping

</td><td>

Customizes the levels mapped to various types of vulnerabilities so that they can be represented in the Vulnerabilities widget in the [Release Quality dashboard](../concept/dpr-release-quality-dashboard.md).

</td></tr><tr><td>

sn\_dpr\_model.release\_related\_task\_types

</td><td>

Specifies the comma-separated list of Task record types that can be associated with a release. Each entry includes the table name and the default view type, and the name of the list that shows up on the Release scope page of a release.-   Type: string
-   Default value:

    ```
[
{"table":"incident", "view": "default", "label": "Incidents"}, 
{"table":"problem", "view": "default", "label": "Problems"}, 
{"table":"sc_request", "view": "default", "label": "Catalog requests"}
]
    ```

-   Other possible values: Other Task record types in the same format as provided in the default value.

</td></tr><tr><td>

sn\_dpr\_workspace.allowed\_states\_for\_create\_auto\_product\_enhancement

</td><td>

States of primary epics that are considered for automatic creation of product enhancements.-   Type: string
-   Default value: created,planned,wip,complete,proposed,active,design,ready
-   Other possible values: You can provide new states or modify the list of existing states.

</td></tr><tr><td>

sn\_dpr\_workspace.auto\_create\_product\_enhancement\_for\_primary\_epic

</td><td>

Determines whether product enhancements can be automatically created for primary epics.-   Type: true\|false
-   Default value: false
-   Other possible values: true

</td></tr><tr id="dpr-sys-prop-citype"><td>

sn\_dpr\_workspace.cmdb\_model\_creation.supported\_ci\_types

</td><td>

Specifies the comma-separated list of Configuration Item \(CI\) types that can be associated with products or services while requesting them. For more information, see [Request a new product or service](../task/dpr-request-product.md).

</td></tr></tbody>
</table>**Parent Topic:**[Digital Product Release reference](../concept/dpr-reference.md)

