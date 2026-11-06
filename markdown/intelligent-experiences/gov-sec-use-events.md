---
title: Monitor AI asset security events and recommendations
description: Triage and resolve AI recommendations and AI asset security events to optimize AI asset security.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-sec-use-events.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Managing AI asset security, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Monitor AI asset security events and recommendations

Triage and resolve AI recommendations and AI asset security events to optimize AI asset security.

## Before you begin

Role required: AI steward \[sn\_ai\_governance.ai\_steward\]

## Procedure

1.  Navigate to **AI Control Tower** &gt; **Govern** &gt; **Security**.

2.  On the **Overview** tab, go to Your top recommendations.

    **Note:** In a domain-separated instance, Your top recommendations isn't shown. Instead, go to Security events detected to review AI asset security events.

3.  In Your top recommendations, review the AI recommendations and security tasks assigned to you.

    Confirm that these recommendations align with your specific needs before taking action.

4.  On any AI recommendation, select **Open** to view all associated AI asset security events.

    To mark a recommendation as resolved, select **Complete**. To remove it, select **Delete** and confirm. You can't restore a deleted recommendation. For more information, see [Activity Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-activity-center.md).

5.  On any AI asset security event, select an option from the Actions menu.

<table id="choicetable_kbs_cjn_1lc"><tbody><tr><td id="d359626e144">

**__Create Asset Task__ \(shown as __Create SIR__ if the Security Incident Response plugin is installed\)**

</td><td>

Create a task to remediate the security event.

</td></tr><tr><td id="d359626e158">

**__View asset details__**

</td><td>

View the asset record in inventory.

</td></tr><tr><td id="d359626e168">

**__View containment options__**

</td><td>

Review AI agent containment \(kill switch\), such as deactivating the agent.

</td></tr><tr><td id="d359626e178">

**__View source log__**

</td><td>

See the input, output, and reason the security event was captured. Sensitive data, such as credit card numbers, are masked. You can also view the source trace record for the event.

</td></tr><tr><td id="d359626e191">

**__View map__**

</td><td>

See the AI asset in the agent map.

</td></tr></tbody>
</table>    The Incident column shows the task linked to the security event, if it exists. To find events, search the list by keyword, or filter it by category, threat type, AI asset, provider, detected date range, or severity. If you view asset details for an AI agent, and it has malicious activity detected, a banner appears.

    \[Omitted image "gov-sec-malicious-activity-banner.png"\] Alt text: Banner indicating that malicious activity was detected for the AI agent.

6.  In the malicious activity banner, select **View containment options** to address the AI agent issue.

    For more information, see [Contain AI agents manually using kill switch protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.md).


