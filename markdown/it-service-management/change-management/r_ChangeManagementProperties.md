---
title: Change Management properties
description: Administrators can use change properties to configure Change Management behavior.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Change Management, IT Service Management]
---

# Change Management properties

Administrators can use change properties to configure Change Management behavior.

Navigate to **Change** &gt; **Administration** &gt; **Change Properties** to view and edit these properties.

<table id="table_qc3_qt4_p4"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.approval\_engine.change\_task

</td><td>

Change request tasks approval engine.-   Type: choice list
-   Default value: process\_guide

</td></tr><tr><td>

glide.ui.risk\_calculate\_rule

</td><td>

Change risk calculation method. Business rule calculates on insert/update, UI action calculates only on demand. **None** disables this capability.-   Type: choice list
-   Default value: ui\_action

 For more information, see [Risk Calculator property](../../../script/server-scripting/reference/r_ChangeRiskCalculator.md).

</td></tr><tr><td>

com.snc.change\_request.enable\_copy

</td><td>

Enable copy change feature.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

com.snc.change\_request.copy.attributes

</td><td>

List of attributes \(comma-separated\) that are copied from the originating change.-   Type: string
-   Default value: category,cmdb\_ci,priority,risk,impact,type,assignment\_group,assigned\_to,short\_description,description,change\_plan,backout\_plan,test\_plan

</td></tr><tr><td>

com.snc.change\_request.copy.rl.change\_task.attributes

</td><td>

List of attributes \(comma-separated\) from the Change Task \[change\_task\] related list that will be copied from the originating change.-   Type: string
-   Default value: cmdb\_ci,priority,assignment\_group,assigned\_to,short\_description,description

</td></tr><tr><td>

com.snc.change\_request.copy.rl.task\_ci.attributes

</td><td>

List of attributes \(comma-separated\) from the Affected CIs \[task\_ci\] related list that will be copied from the originating change.-   Type: string
-   Default value: ci\_item

</td></tr><tr><td>

com.snc.change\_request.attach.enable\_copy

</td><td>

Copy attachments from the originating change.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

com.snc.change\_request.copy.rl.task\_cmdb\_ci\_service.attributes

</td><td>

List of attributes \(comma-separated\) from Impacted Services \[task\_cmdb\_ci\_service\] related list that will be copied from the originating change.-   Type: string
-   Default value: cmdb\_ci\_service

</td></tr><tr><td>

com.snc.task.refresh\_impacted\_services

</td><td>

List of all the Task types where **Refresh Impacted Services** action is enabled.-   Type: string
-   Default value: incident, change\_request

</td></tr><tr><td>

change.refresh\_impacted.include\_affected\_cis

</td><td>

Lists the impacted CIs or Services with any service supported by a configuration item identified in the Affected CI related list. **Note:** This requires any business services identified to be converted to an application service. For instructions, see [Convert business services to application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/convert-bus-to-app-svc-intro.md). For information about application services, see [Application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/application-services.md).

</td></tr><tr><td>

com.snc.change\_management.enforce\_data\_requirements

</td><td>

Enforce change request process data requirements, so that any data modification on the change request has the same data restrictions. This includes, updates made through the change request form, Workflow, REST/SOAP, JavaScript, and GlideRecord updates. For more information, see [Change Management API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/change-management-api.md)

 In the User Interface, when this property is true, it enables additional server sided restrictions to the UI Policy and Client Script controls that already exist.

 -   Type: true \| false
-   Default value: true

</td></tr><tr><td>

com.snc.task.populate\_service\_offering

</td><td>

Populates the service offering related list from the impacted service list.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

com.snc.change\_request.enable\_unauthorized

</td><td>

Enables the creation of unauthorized change requests when the event **ci.change.unplanned** is raised.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

com.snc.change\_request.event.state\_updated.enabled

</td><td>

Generates the **sn\_change.state.updated** event when the state of the change request is updated.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

com.snc.change\_request.event.state\_updated.states

</td><td>

Enter the change request state field values, each separated by a comma to generate the **sn\_change.state.updated** event. This happens when any of the state value changes, for example, -5, -3, 0. You can leave the property empty to generate the **sn\_change.state.updated** event for all state changes. For more information on the state values, see [Legacy: State model and transitions](../concept/c_ChangeStateModel.md).**Note:** For this property to take effect, property **com.snc.change\_request.event.state\_updated.enabled** must be set to true.

</td></tr></tbody>
</table>## Change Management properties for Discovery integration

If your organization is subscribed to Discovery , integration with Discovery is automatically enabled. With this integration, any configuration item \(CI\) with an IP address that is part of a change request process can be maintained automatically. When Discovery is activated, the following three new properties become available.

<table id="table_mh3_5wb_4gb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.change\_request.auto.discovery

</td><td>

Trigger Discovery for the Affected CIs automatically, manually or not at all.-   Type: Choice list
-   Values: Off, Both, Automatic, Manual
-   Default value: Off

</td></tr><tr><td>

com.snc.change\_request.disco.auto.state

</td><td>

Defines which Change Request states Discovery will be automatically triggered.-   Type: String
-   Default value: Review

</td></tr><tr><td>

com.snc.change\_request.disco.manual.state

</td><td>

Defines which Change Request states allow Discovery to be manually triggered.-   Type: String
-   Default value: Implement, Review

</td></tr></tbody>
</table>## Change Management properties available from sys\_properties table

The following properties are available for further configuration. To list them, enter `sys_properties.list` in the navigator text box and filter for **com.snc.change\_**.

<table id="table_ax1_nvt_yr"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.change\_request.copy.related\_lists

</td><td>

Related lists \(comma-separated\) that will be copied from the originating change.-   Type: string
-   Default value: task\_ci,task\_cmdb\_ci\_service,change\_task

</td></tr><tr><td>

com.snc.change\_request.rl.change\_task.attach.enable\_copy

</td><td>

Copy attachments from originating change task.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

com.snc.change\_management.policy.approval.log

</td><td>

The debug logging property that provides the detailed logging information of the workflow activity when using Change Approval Policies.Type: choice list

</td></tr><tr><td>

sn\_change\_cab.com.snc.change\_management.cab.use\_sow\_meeting

</td><td>

Controls opening of a CAB meeting from the CAB Meeting calendar in the CAB Workbench in Service Operations Workspace.**Note:** Users must have the sn\_sow.sow\_user role to open CAB meetings in SOW.

-   Type: true \| false
-   Default value: false, for upgrade customers; true for new customers.

-   **true**: CAB meetings open in the CAB Meeting workbench in SOW.
-   **false**: CAB meetings open in the Core UI.

</td></tr></tbody>
</table>**Parent Topic:**[Reference section for Change Management](../concept/reference-change-management.md)

