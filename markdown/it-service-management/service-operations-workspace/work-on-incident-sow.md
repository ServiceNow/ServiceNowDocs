---
title: Work on an incident record in Service Operations Workspace
description: If resolving the incident involves creating a problem, change, service request, and so on, you can create them directly from the incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/work-on-incident-sow.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Incident Management in Service Operations Workspace, Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Work on an incident record in Service Operations Workspace

If resolving the incident involves creating a problem, change, service request, and so on, you can create them directly from the incident record.

## Before you begin

Role required: itil, sn\_service\_desk\_agent

## Procedure

1.  Open an incident.

    For information about creating an incident in Service Operations Workspace, see [Create an incident in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-incident-sow.md).

2.  Perform any of the following actions on the incident record page.

<table id="choicetable_hvj_ccg_vsb"><thead><tr><th align="left" id="d76162e71">

Option

</th><th align="left" id="d76162e74">

Description

</th></tr></thead><tbody><tr><td id="d76162e80">

**Create a change request**

</td><td>

Select **Create change request**. See [Create a change request in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-change-sow.md).

</td></tr><tr><td id="d76162e99">

**Create an incident task**

</td><td>

From the drop-down next to **Create incident task**, select **Create incident task**.

</td></tr><tr><td id="d76162e114">

**Create an outage**

</td><td>

From the drop-down next to **Create outage**, select **Create outage**.

</td></tr><tr><td id="d76162e129">

**Create a problem**

</td><td>

From the drop-down next to **Create problem**, select **Create problem**. See [Create a problem in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-problem-sow.md).

</td></tr><tr><td id="d76162e152">

**Create a request**

</td><td>

From the drop-down next to **Create request**, select **Create request**. See [Create a catalog request in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-catalog-request-sow.md).

</td></tr><tr><td id="d76162e180">

**Resolve the incident**

</td><td>

Select **Resolve** and provide the resolution code and notes.

</td></tr><tr><td id="d76162e192">

**Assign the incident to you**

</td><td>

Select **Assign to me**.

</td></tr><tr><td id="d76162e204">

**Book a walk-up appointment**

</td><td>

Select the **More actions** icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and then select **Book Walk-up Appointment**.

</td></tr><tr><td id="d76162e225">

**Compose an email**

</td><td>

Select the **More actions** icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and then select **Compose Email**.

</td></tr><tr><td id="d76162e246">

**Copy the record page URL to easily access the record**

</td><td>

Select the **More actions** icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and then select **Copy URL**. You can then share the URL with other agents.

</td></tr><tr><td id="d76162e268">

**Copy the incident**

</td><td>

Select the **More actions** icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and then select **Copy Incident**.

</td></tr><tr><td id="d76162e289">

**Promote the incident to major incident**

</td><td>

Select the **More actions** icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and then select **Promote to Major Incident**.

</td></tr><tr><td id="d76162e310">

**Propose the incident as major incident**

</td><td>

Select the **More actions** icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and then select **Propose Major Incident**.

</td></tr><tr><td id="d76162e331">

**Report knowledge gap**

</td><td>

Select the **More actions** icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and then select **Report Knowledge Gap** to create a Knowledge Feedback Task \(KFT\) record. When the record is created, the success message containing the link to the KFT record, is displayed. You can select the link to open the KFT record on a separate tab within the incident view. You can also view the KFT record from the Knowledge Gaps related list on the **Related records** tab. You can use the KFT record to create a knowledge article.

</td></tr><tr><td id="d76162e357">

**Delete the incident**

</td><td>

Select the **More actions** icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and then select **Delete**.

</td></tr><tr><td id="d76162e378">

**View recommendations for the incident**

</td><td>

From the contextual side panel, select the **Recommendations** icon \(\[Omitted image "recommendation-icon.png"\] Alt text: recommendations icon\). See [Recommendation Framework in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/recommendation-framework-sow.md).

</td></tr><tr><td id="d76162e404">

**View record information and perform relevant actions**

</td><td>

From the contextual side panel, select the **Record Information** icon \(\[Omitted image "record-info-icon.png"\] Alt text: record Information icon\).Select the **Contact** option to view the caller information such as name, location \(address\), email id and so on.

 The following options are available based on the **Assignment group** and **Assigned to** fields of the incident.

-   Assign to me: When the **Assignment group** field is empty and the logged-in user is a member of the current assignment group.

If the logged-in user is a member of multiple assignment groups, select the required assignment group while assigning the incident.

-   Assign: When the logged-in user is not a member of the current assignment group.
-   Reassign

    -   When only the **Assigned to** field is populated with the logged-in user.
    -   When both **Assignment group** and **Assigned to** \(as logged-in user\) fields are populated.
If the logged-in user is a member of multiple assignment groups, the following scenarios are possible when changing the assignment group.

    -   If the user is a member of that assignment group, the **Assigned to** field retains the logged-in user.
    -   If the user is not a member of that assignment group, the **Assigned to** field becomes empty.
For more information, see [Viewing incident record information using the Contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/view-inc-record-info-contextual-sidepanel.md).

</td></tr><tr><td id="d76162e495">

**Attach a record that helps in quick resolution of the change**

</td><td>

1.  From the contextual side panel, select the **Agent assist** icon \(\[Omitted image "agent-assist-icon.png"\] Alt text: agent assist icon\).
2.  Search for a resource and perform the required action, for example, link the change to an incident.


</td></tr><tr><td id="d76162e522">

**Reach out to experts on-call**

</td><td>

From the contextual side panel, select the **Experts on-call** icon \(\[Omitted image "experts-on-call.png"\] Alt text: experts on-call icon\). See [On-call support for an incident in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/on-call-sow.md).

</td></tr><tr><td id="d76162e547">

**View dynamic tracking of an on-call escalation**

</td><td>

From the contextual side panel, select the **On-call escalations** icon \[Omitted image "on-call-escalation.png"\] Alt text: on-call escalations icon\). See [On-call support for an incident in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/on-call-sow.md).

</td></tr><tr><td id="d76162e572">

**Collaborate using Microsoft Teams**

</td><td>

From the contextual side panel, select the **Collaborate** icon \(\[Omitted image "collaborate-sidebar.png"\] Alt text: collaborate icon\). See [ServiceNow integrations with Microsoft Teams in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/msteams-sow.md).

</td></tr><tr><td id="d76162e609">

**Add attachments**

</td><td>

From the contextual side panel, select the **Attachments** icon \(\[Omitted image "attachment-icon.png"\] Alt text: attachments icon\).**Note:** The added attachments are displayed in the activity stream in the **Compose** section.

</td></tr><tr><td id="d76162e634">

**Action library**

</td><td>

From the contextual side panel, select the **Action library** \(\[Omitted image "icon-action-library.png"\]\) icon to open a sidepanel that contains all the DEX actions that you can perform on the CIs such as clearing the cache.**Note:** You can perform DEX actions on the affected CIs or caller CIs that are associated with the incident record. The caller CIs are the CIs that are assigned to the caller.

</td></tr><tr><td id="d76162e656">

**Create templates for reuse**

</td><td>

From the contextual side panel, select the **Templates** icon \(\[Omitted image "template-icon.png"\] Alt text: templates icon\) and create a template or reuse an existing one.

</td></tr><tr><td id="d76162e674">

**Playbook**

</td><td>

From the contextual side panel, select the **Playbook** icon \(\[Omitted image "playbook\_icon.png"\] Alt text: Playbook icon\) to open the playbook and execute the remedial actions on a separate panel. For more information, see [Remedial actions using Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/remedial-actions-playbook.md).

</td></tr><tr><td id="d76162e699">

**Response templates**

</td><td>

From the contextual side panel, select the **Response template** icon \(\[Omitted image "sow-response-template-icon.png"\] Alt text: Response template icon\) to open and use available the response message templates as reusable messages that you can copy and paste in the required areas such as email or chat for a quick response. To use the response template feature, the users must have the sn\_templated\_snip.template\_snippet\_reader role. Some of the response templates available in the base system include Need more information and Schedule meeting response templates. The response templates can be used with communication channels such as form channel, SMS and email. For more information on defining and configuring the response templates for incident tables in Service Operations Workspace, see [Response templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/response-templates-templated-snippets.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Incident Management in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/incident-sow.md)

**Related topics**  


[Create an incident in Service Operations Workspace]()

[View and update incident information on the Overview tab in SOW]()

[Viewing incident record information using the Contextual side panel]()

[Work on an incident list page in Service Operations Workspace]()

[Remedial actions using Playbook]()

[Close resolved incident]()

[Reopen an incident in Service Operations Workspace]()

[Incident Management in Service Operations Workspace reference]()

