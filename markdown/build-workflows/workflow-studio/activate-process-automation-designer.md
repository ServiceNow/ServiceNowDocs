---
title: Activate playbooks
description: Activate the Workflow Studio application to create flows, playbooks, and more for any of your use cases.Activate Playbooks on your instance to create playbooks in App Engine.Activate Workflow Studio Playbooks on your instance so that you can create Playbooks triggered by CSM tables.Activate Workflow Studio Playbooks on your instance so that you can create Playbooks triggered by tables.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Playbooks, Configure, Workflow Studio, Build workflows]
---

# Activate playbooks

Activate the Workflow Studio application to create flows, playbooks, and more for any of your use cases.

Playbooks are included with Workflow Studio, which is a ServiceNow AI Platform feature that is active by default, and that is available for installation and update from the ServiceNow Store. However, you can only trigger playbooks off of platform and application tables that you have access to. These can be:

-   Application tables
-   Custom tables that extend the application tables
-   Custom tables authorized by the application subscription

Each application subscription entitles you to create playbooks for its associated tables. Purchase subscriptions to access any additional tables that you want to trigger your playbooks from. If you already have a subscription to your application but you still can't create playbooks for your application's tables, enable the appropriate plugin.

**Note:** The plugins you enable determine which tables are available for you to create playbooks.

See the following sections to learn how to activate Workflow Studio Playbooks for your application.

**Parent Topic:**[Configuring playbooks](setting-up-process-automation-designer.md)

## Activate Playbooks for App Engine

Activate Playbooks on your instance to create playbooks in App Engine.

### Before you begin

Role required: admin

### About this task

In order to create playbooks in App Engine, you must [purchase a subscription to the ServiceNow AI Platform App Engine](https://www.servicenow.com/now-platform/app-engine/pricing.html).

To purchase this subscription, contact your ServiceNow account manager. Your account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps to enable the **Process Automation Designer for App Engine \[com.glide.pad.license\]** plugin:

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

3.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Select the instance that you want to activate the plugin on.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Select the name of the plugin to activate.

 **Note:** If the system doesn't list the plugin you want or if you're activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


### Result

You can create triggers in Playbooks for [custom tables that you create](https://www.servicenow.com/docs/access?context=t_CreateATable&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US). Enabling the **Process Automation Designer for App Engine \[com.glide.pad.license\]** plugin lets you create playbooks for these tables and their [extensions](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US):

-   Affected CIs \[cmdb\_outage\_ci\_mtom\]
-   Agent Capacity \[awa\_agent\_capacity\]
-   Agent channel availability \[awa\_agent\_channel\_availability\]
-   Agent Presence \[awa\_agent\_presence\]
-   Announcement \[announcement\]
-   Assessment Category Result \[asmt\_category\_result\]
-   Assessment Instance \[asmt\_assessment\_instance\]
-   Assessment Metric \[asmt\_metric\]
-   Assessment Metric Template \[asmt\_template\]
-   Assessment Metric Type \[asmt\_metric\_type\]
-   Assessment Metric Type Group \[asmt\_metric\_type\_group\]
-   Assessment Net Promoter Score \[asmt\_nps\_result\]
-   Assessment Template Definition \[asmt\_template\_definition\]
-   Assignment Eligibility \[awa\_eligibility\_pool\]
-   Assignment Rule \[awa\_assignment\_rule\]
-   Audit \[cert\_audit\]
-   Audit Result \[cert\_audit\_result\]
-   AWA Agent Presence and Capacity \[awa\_agent\_presence\_capacity\]
-   AWA Document Size \[awa\_document\_size\]
-   Base Configuration Item \[cmdb\]
-   Building \[cmn\_building\]
-   Business Calendar \[business\_calendar\]
-   Certification Template \[cert\_template\]
-   CI Relation Filter \[cmdb\_rel\_filter\]
-   CI Relationship \[cmdb\_rel\_ci\]
-   CI Relationship Rollup \[cmdb\_rel\_rollup\]
-   CI Relationship Type \[cmdb\_rel\_type\]
-   CI/User Relationship Type \[cmdb\_rel\_user\_type\]
-   CIs Affected \[task\_ci\]
-   CMDB Group \[cmdb\_group\]
-   CMDB Group Event Queue \[cmdb\_group\_event\_queue\]
-   CMDB Group Type \[cmdb\_group\_type\]
-   CMDB Health Configuration \[cmdb\_health\_config\]
-   CMDB Health Metric \[cmdb\_health\_metric\]
-   CMDB Health Result \[cmdb\_health\_result\]
-   CMDB Health Scorecard \[cmdb\_health\_scorecard\]
-   Company \[core\_company\]
-   Connection &amp; Credential Aliases \[sys\_alias\]
-   Connection &amp; Credential Templates \[sys\_alias\_templates\]
-   Cost Center \[cmn\_cost\_center\]
-   Country \[core\_country\]
-   Department \[cmn\_department\]
-   Direct Relationships \[cmdb\_related\]
-   \[dms\_document\]
-   Draft Document \[draft\_document\]
-   Follow On Task \[cert\_follow\_on\_task\]
-   Group \[sys\_user\_group\]
-   Group Member \[sys\_user\_grmember\]
-   Group Queue Priority \[awa\_group\_queue\_priority\]
-   Group Relationship \[cmdb\_rel\_group\]
-   Group Role \[sys\_group\_has\_role\]
-   Group Skill \[sys\_group\_has\_skill\]
-   Guided Setup Task \[gsw\_task\]
-   Holiday \[sys\_holiday\]
-   Impacted CIs \[task\_cmdb\_ci\_service\]
-   Inbox Layout \[awa\_inbox\_layout\]
-   Interaction \[interaction\]
-   IP Address Pool \[cmdb\_ip\_address\_pool\]
-   IP Address Range \[cmdb\_ip\_address\_range\]
-   IP Address to DNS Name \[cmdb\_ip\_address\_dns\_name\]
-   IP Service \[cmdb\_ip\_service\]
-   KB Submission \[kb\_submission\]
-   Knowledge \[kb\_knowledge\]
-   Knowledge Base \[kb\_knowledge\_base\]
-   Knowledge Category \[kb\_category\]
-   Knowledge Feedback \[kb\_feedback\]
-   Knowledge Feedback Task \[kb\_feedback\_task\]
-   Knowledge Use \[kb\_use\]
-   Location \[cmn\_location\]
-   Metric \[metric\_instance\]
-   Model Category \[cmdb\_model\_category\]
-   Offer Details \[awa\_offer\_details\]
-   OS User \[cmdb\_os\_user\]
-   Outage \[cmdb\_ci\_outage\]
-   Page \[sp\_page\]
-   Peer Relationships \[cmdb\_peer\]
-   People Relationship \[cmdb\_rel\_person\]
-   Presence State \[awa\_presence\_state\]
-   Private Task \[vtb\_task\]
-   Product Model \[cmdb\_model\]
-   Queue \[awa\_queue\]
-   Related Entry \[cmdb\_related\_entry\]
-   Report \[sys\_report\]
-   Role \[sys\_user\_role\]
-   Roster \[cmn\_rota\_roster\]
-   Rotation Escalation \[cmn\_rota\_escalation\]
-   Scheduled Suite Run \[sys\_atf\_schedule\_run\]
-   Service \[cmdb\_ip\_service\_ci\]
-   Service Portal \[sp\_portal\]
-   Shift \[cmn\_rota\]
-   Shift Escalation Set \[cmn\_rota\_escalation\_set\]
-   Shift Escalation Step Definition \[cmn\_rota\_esc\_step\_def\]
-   Skill Category \[cmn\_skill\_category\]
-   Skill Level \[cmn\_skill\_level\]
-   Skill Level Type \[cmn\_skill\_level\_type\]
-   Subscribers \[cmdb\_subscriber\]
-   Template \[sys\_template\]
-   Test \[sys\_atf\_test\]
-   Test Results \[sys\_atf\_test\_result\]
-   Test Suite \[sys\_atf\_test\_suite\]
-   Test Suite Result \[sys\_atf\_test\_suite\_result\]
-   Test Suite Test \[sys\_atf\_test\_suite\_test\]
-   Test Template \[sys\_atf\_test\_template\]
-   Theme \[sp\_theme\]
-   Ticket \[ticket\]
-   \[universal\_request\]
-   User \[sys\_user\]
-   User Skill \[sys\_user\_has\_skill\]
-   Vendor Type \[vendor\_type\]
-   Work Item \[awa\_work\_item\]
-   Work Item Rejection \[awa\_work\_item\_rejection\]
-   Work Item Sizing \[awa\_work\_item\_sizing\]
-   Work Item Sort Order \[awa\_queue\_item\_sorting\]

**Note:** If you create a custom table such as My Table \[x\_my\_table\], you can create playbooks that trigger from it. However, you cannot create a playbook that triggers from a table belonging to another Process Automation Designer plugin.

## Activate Playbooks for Customer Service Management \(CSM\)

Activate Workflow Studio Playbooks on your instance so that you can create Playbooks triggered by CSM tables.

### Before you begin

Role required: admin

### About this task

In order to create Playbooks in Workflow Studio that are triggered by CSM tables and custom tables that extend from them, you need to [purchase a subscription to CSM](https://www.servicenow.com/lpgp/pricing-csm.html).

To purchase this subscription, contact your ServiceNow account manager. Your account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps to enable the **Playbooks for Customer Service Management \[com.sn\_csm\_playbook\]** plugin:

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

3.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Select the instance that you want to activate the plugin on.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Select the name of the plugin to activate.

 **Note:** If the system doesn't list the plugin you want or if you're activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


### Result

Enabling the **Playbooks for Customer Service Management \[com.sn\_csm\_playbook\]** plugin lets you create playbooks for these tables and their [extensions](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US):

-   Account \[customer\_account\]
-   Case \[sn\_customerservice\_case\]
-   Change Request \[change\_request\]. Requires Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Consumer \[csm\_consumer\]
-   Contact \[customer\_contact\]
-   Escalation \[sn\_customerservice\_escalation\]
-   Household \[csm\_household\]
-   Incident \[incident\]. Requires Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Interaction \[interaction\]
-   Order \[csm\_order\]. Requires Customer Service Management for Orders \(com.snc.csm.order\)
-   Order Line Item \[csm\_order\_line\_item\]. Requires Customer Service Management for Orders \(com.snc.csm.order\)
-   Problem \[problem\]. Requires Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Request \[sc\_request\]. Requires Customer Service with Request Management \(com.sn\_cs\_sm\_request\)
-   Service Organization \[sn\_customer\_service\_organization\]. Requires Service Organization \(com.snc.service\_organization\)
-   Task \[sn\_customerservice\_task\]

**Note:** If you create a custom table that extends a CSM table such as Case, you can create playbooks that trigger from it.

## Activate Playbooks for Field Service Management

Activate Workflow Studio Playbooks on your instance so that you can create Playbooks triggered by tables.

### Before you begin

Role required: Admin.

### About this task

In order to create Playbooks in Workflow Studio that are triggered by Field Service Management tables, you must [purchase a subscription to Field Service Management](https://www.servicenow.com/lpgp/pricing-field-service-management.html).

To purchase this subscription, contact your ServiceNow account manager. Your account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps to enable the **Playbooks for Field Service Management \[com.sn\_fsm\_playbook\]** plugin:

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

3.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Select the instance that you want to activate the plugin on.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Select the name of the plugin to activate.

 **Note:** If the system doesn't list the plugin you want or if you're activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


### Result

Enabling the **Playbooks for Field Service Management \[com.sn\_fsm\_playbook\]** plugin lets you create Playbooks for these tables and their [extensions](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US):

-   Work Task Flow \[sf\_work\_task\]
-   Work Order Flow \[sf\_work\_order\]
-   Work Order Task \[wm\_Task\]
-   Work Order \[wm\_order\]
-   Work Order Model \[cmdb\_workorder\_product\_model\]
-   Work Task Model \[cmdb\_worktask\_product\_model\]
-   Work Type \[wm\_work\_type\]
-   Agent Personal Schedule \[agent\_events\]
-   Appointment Booking \[sn\_apptmnt\_booking\_appointment\_booking\]
-   Questionnaire \[wm\_questionnaire\]
-   Service Order Task \[sm\_task\]
-   Service Order Task Template Dependency \[sm\_m2m\_task\_template\_dependency\]
-   Asset Usage \[sm\_asset\_usage\]
-   Part Requirement \[sm\_part\_requirement\]
-   Service Management Incidentals \[sm\_incidentals\]

