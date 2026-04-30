---
title: Incident Management properties
description: Incident Management properties are used to control features such as copying and creating child incidents. The major incident properties control the promotion of major incident candidates to major incidents.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configure, Incident Management, IT Service Management]
---

# Incident Management properties

Incident Management properties are used to control features such as copying and creating child incidents. The major incident properties control the promotion of major incident candidates to major incidents.

These properties are available at **Incident** &gt; **Administration** &gt; **Incident Properties**.

<table id="table_cmc_hbh_fbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Incident closure properties

</td></tr><tr><td>

Enable auto closure of incidents based on Resolution date. Setting this to 'No' will make auto closure to run based on the Updated date.\(com.snc.incident.autoclose.basedon.resolved\_at\)

</td><td>

Select the check box to auto-close incidents based on the resolution date of the incident instead of the last updated date. **Note:** Starting with the Madrid release, this property is automatically set to **true** for new customers. Existing customers have to set the property to **true** manually.

</td></tr><tr><td>

Number of days \(integer\) after which Resolved incidents are automatically closed. Zero \(0\) disables this feature \(glide.ui.autoclose.time\)

</td><td>

Set the duration of the incident auto-close function.

</td></tr><tr><td>

Close open Incident Tasks when Incident is closed or canceled\(com.snc.incident.incident\_task.closure\)

</td><td>

Select the check box to close an open incident task when an incident is closed or canceled.**Note:** Starting with the Madrid release, this property is automatically set to **true** by default only for the new customers.

</td></tr><tr><td>

Close open Incident Communication Plans when Incident is closed or canceled\(com.snc.incident.incident\_alert.closure\)

</td><td>

Select the check box to close an open incident communication plan when an incident is closed or canceled. **Note:** This property is visible when the Incident Communications Management plugin \(com.snc.iam\) is enabled. This property is set to **false** for both new and existing customers.

</td></tr><tr><td>

Close open Incident Communication Tasks when an Incident Communication Plan is closed or canceled\(com.snc.iam.incident\_alert\_task.closure\)

</td><td>

Select the check box to close an open incident communication task when an incident communication plan is closed or canceled. **Note:** This property is visible when the Incident Communications Management plugin \(com.snc.iam\) is enabled. This property is set to **false** for both new and existing customers.

</td></tr><tr><td class="sub-head" colspan="2">

Incident reopen properties

</td></tr><tr><td>

List of fields \(comma-separated\) to copy from the original incident when an incident is reopened by email \(com.snc.incident.clone\_fields\_on\_reopen\)

</td><td>

Enter the name of the fields that you want to be copied from the original incident to the new incident when you reopen an incident through email. **Note:** When an incident is reopened, a new incident is created.

</td></tr><tr><td class="sub-head" colspan="2">

Copy incident and create child incident properties

</td></tr><tr><td>

Enable copy incident feature\(com.snc.incident.copy.enable\)

</td><td>

Select the check box to enable the **Copy Incident** option in the context menu.

</td></tr><tr><td>

Enable create child incident feature\(com.snc.incident.create.child.enable\)

</td><td>

Select the check box to enable the **Create Incident** option in the context menu.

</td></tr><tr><td>

Copy attachments from originating incident\(com.snc.incident.copy.attach\)

</td><td>

Select the check box to be able to copy attachments from original incidents when an incident is copied for created.

</td></tr><tr><td>

List of attributes \(comma-separated\) that will be copied from the originating incident\(com.snc.incident.copy.attributes\)

</td><td>

Enter the name of the attributes that you want to be copied from the original incident to the new incident when you copy or create an incident. **Note:** The knowledge article or the resolution section information such as resolution code, notes, and resolved by, isn’t copied.

</td></tr><tr><td>

Related lists \(comma-separated\) that will be copied from the originating incident \(com.snc.incident.copy.related\_lists\)

</td><td>

Enter the name of the related lists that you want to be copied from the original incident to the new incident when you copy or create an incident.

</td></tr><tr><td>

List of attributes \(comma-separated\) from Affected CIs \(task\_ci\) related list that will be copied from the originating incident \(com.snc.incident.copy.rl.task\_ci.attributes\)

</td><td>

Enter the name of the attributes from the Affected CIs related list that you want to be copied from the original incident to the new incident when you copy or create an incident.

</td></tr><tr><td>

List of attributes \(comma-separated\) from Impacted Services \(task\_cmdb\_ci\_service\) related list that will be copied from the originating incident \(com.snc.incident.copy.rl.task\_cmdb\_ci\_services.attributes\)

</td><td>

Enter the name of the attributes from the Impacted Services related list that you want to be copied from the original incident to the new incident when you copy or create an incident.

</td></tr><tr><td class="sub-head" colspan="2">

Incident form fields configuration properties

</td></tr><tr><td>

List of fields \(comma-separated\) that appear in the activity formatter for Incident \(glide.ui.incident\_activity.fields\)

</td><td>

Enter the names of the fields that become visible in the activity formatter. If the activities are personalized, this property updates automatically.

</td></tr><tr><td>

Additional comments icon used in Task Activity formatter \(glide.ui.incident\_activity.image.comments\)

</td><td>

Enter the path of the icon that is used for additional comments.

</td></tr><tr><td>

Work notes icon used in Task Activity formatter \(glide.ui.incident\_activity.image.work\_notes\)

</td><td>

Enter the path of the icon that is used for work notes.

</td></tr><tr><td>

Incident additional comments style \(glide.ui.incident\_activity.style.comments\)

</td><td>

Enter the HTML syntax of comment style for incident additional comments.

</td></tr><tr><td>

Incident work notes style \(glide.ui.incident\_activity.style.work\_notes\)

</td><td>

Enter the HTML syntax of work notes style for incident additional comments.

</td></tr><tr><td class="sub-head" colspan="2">

Incident created from interaction properties

</td></tr><tr><td>

Create Incident in saved state from Interaction\(com.snc.incident.create\_from\_interaction.save\)

</td><td>

Select the check box to create an incident with a saved state from an interaction record.Type: Boolean

 **Note:** Starting with the Xanadu release, this property is automatically set to **true** for new customers. Existing customers have to set the property to **true** manually.

</td></tr><tr><td>

Copy attachments from Interaction to Incident, when created from Interaction\(com.snc.incident.create\_from\_interaction.copy\_attachments\)

</td><td>

Select the check box to copy the attachments from the interaction record to a new incident record when it's created from the interaction record.Type: Boolean

 **Note:** Starting with the Xanadu release, this property is automatically set to **true** for new customers. Existing customers have to set the property to **true** manually.

</td></tr></tbody>
</table>## Major Incident Management

If you have the admin or incident\_manager role, you can edit the major incident properties. You can define whether a new major incident must be created or whether a major incident candidate must be promoted to a major incident. The properties are available only when you activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\).

These properties are available at **Incident** &gt; **Administration** &gt; **Major Incident Properties**.

<table id="table_upp_kdq_kbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create major incident from candidate\(sn\_major\_inc\_mgmt.com.snc.incident .mim.major\_incident\_creation\)

</td><td>

Create a new major incident or promote a major incident candidate to a major incident.**Note:** When a new major incident is created from an incident, the current incident is marked as a child of the new major incident.

</td></tr><tr><td>

Compose Email on Major Incident Overview\(sn\_major\_inc\_mgmt.com.snc.incident.mim.compose\_email\_on\_iatasks\)

</td><td>

Provide a comma-separated list of incident communication task types that can have the **Compose Email** option on the Major Incident Workbench.

</td></tr><tr><td>

PIR export ui page url\(sn\_major\_inc\_mgmt.pir\_export\_pdf\_ui\_page\)

</td><td>

Associate a custom UI page to an exported post incident report.

</td></tr><tr><td>

Major Incident Management Group \(sys\_id\) to whom the Major Incident should be re-assigned on promotion to 'Major Incident'\(sn\_major\_inc\_mgmt.major\_incident\_management\_group\)

</td><td>

Auto-assign a major incident to different assignment groups based on the actions taken on the incidents and the conditions related to the assignment group.

</td></tr><tr><td>

Default recipient location of emails for Communication Tasks\(sn\_comm\_management.default\_email\_recipient\_field\)

</td><td>

Select the default recipient location of emails for communication tasks. The default value is **BCC**.

</td></tr><tr><td>

Property to toggle support for Recipient List on Email Client, on Communication Tasks\(sn\_comm\_management.email\_client\_recipient\_items\_enabled\)

</td><td>

Use the recipient list to send emails as part of the communication tasks.

</td></tr><tr><td>

List of attributes \(comma-separated\) that will be copied from the child Incident when creating a Major Incident\(sn\_major\_inc\_mgmt.com.snc.major\_incident.create.copy.attributes\)

</td><td>

Select the fields that must be copied from the incident when creating a major incident.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Incident Management](../concept/incident-configuration.md)

