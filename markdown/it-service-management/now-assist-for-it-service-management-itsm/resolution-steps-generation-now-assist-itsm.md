---
title: Suggested steps generation in Now Assist for IT Service Management \(ITSM\)
description: Generate suggested steps automatically by analyzing clusters of closed incidents with similar incident resolution in the Now Assist for IT Service Management \(ITSM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/resolution-steps-generation-now-assist-itsm.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Suggested steps generation in Now Assist for IT Service Management \(ITSM\)

Generate suggested steps automatically by analyzing clusters of closed incidents with similar incident resolution in the Now Assist for IT Service Management \(ITSM\) application.

## Before you begin

**Important:** Starting with the Australia release, the Suggested steps skill is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. This feature is being replaced with [Learning Enhanced Automation Platform \(LEAP\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap.md). For information on how to get started see, [How to get started with LEAP](https://www.servicenow.com/community/itom-articles/leap-learning-enhanced-automation-platform-how-to-get-started/ta-p/3555322).

To transition to LEAP:

1.  Install the LEAP \(sn\_itom\_leap\) plugin.
2.  Activate the LEAP installer skill.

    **Note:** You must be in LEAP scope to activate this skill.

    1.  Go to **Admin** &gt; **Now Assist Admin**.
    2.  Select **Now Assist Skills**.
    3.  In **Technology**, select **ITOM**.
    4.  Activate the LEAP installer plugin.
3.  Add the itil role to access LEAP.
    1.  In the LEAP installer, in the Define access screen, add the itil role in the **Roles** field.\[Omitted image "now-assist-itsm-leap-itil-role.png"\] Alt text: Add itil role in the Roles field
    2.  Select **Save and continue**.

Role required: itil

**Important:** If you are using LEAP, you also need the LEAP agent \(sn\_itom\_leap.leap\_agent\) role. For more information, see [Components installed with LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/components-installed-with-aiops-leap.md).

## About this task

Data from the short description field and the filter conditions set in the incident input table are used to generate the clusters based on similar past resolved incidents. By default, the Suggested steps skills are configured to work with itil roles. With Named Access Accounts \(NAA\), you can restrict access to this skill for a different role. However, itil is still required because the Group-Action framework skills used by **Suggested Steps** enables to access the incidents. For most scenarios, changing the ACL role on Now Assist Admin is sufficient. However, you can also restrict individual skills to specific roles. For information on troubleshooting steps to resolve issues with the Suggested steps generation skill, see [Troubleshoot Suggested steps generation skill set up](https://www.servicenow.com/community/itsm-articles/troubleshooting-steps-for-now-assist-for-itsm-suggested-steps/ta-p/3256267).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace.**

2.  Using the List icon \(\[Omitted image "icon-list.png"\] Alt text: List icon\), open an incident that is not in **Closed** or **Complete** state.

3.  Select the Recommendations icon \(\[Omitted image "now-assist-itsm-recommendations-icon.png"\] Alt text: Output class icon\).

    The steps to resolve the incident appear in a **Recommendations** pop-up window in the incident record. This action may take a few minutes.

<table id="choicetable_mpv_t1l_ljc"><thead><tr><th align="left" id="d119286e236">

If

</th><th align="left" id="d119286e239">

Then

</th></tr></thead><tbody><tr><td id="d119286e245">

**You're using LEAP**

</td><td>

The LEAP Resolution Steps Recommendation will appear.\[Omitted image "now-assist-itsm-recommended-actions-leap.png"\] Alt text: LEAP recommended actions

</td></tr><tr><td id="d119286e262">

**You're using Suggested steps**

</td><td>

The Suggested Steps recommendation will appear.\[Omitted image "now-assist-itsm-suggested-steps.png"\] Alt text: Suggested steps in Now Assist

</td></tr></tbody>
</table>
