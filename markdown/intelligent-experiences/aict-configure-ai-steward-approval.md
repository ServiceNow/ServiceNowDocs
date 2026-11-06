---
title: Require AI steward approval for AI assets
description: Make sure every AI system, MCP server, or AI model is reviewed before deployment by requiring AI steward approval for that asset type and starting approval requests automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-configure-ai-steward-approval.html
release: australia
topic_type: task
last_updated: "2026-11-02"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring builder controls, Configuring ServiceNow AI settings, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Require AI steward approval for AI assets

Make sure every AI system, MCP server, or AI model is reviewed before deployment by requiring AI steward approval for that asset type and starting approval requests automatically.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward or admin

## About this task

Each change takes effect as soon as you select **Activate** or confirm **Deactivate**. There's no separate save step.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **ServiceNow AI**.

2.  Select the **Builder controls** tab.

3.  In the **AI steward approval for AI assets** section, set the approval requirement for each asset type.

<table><thead><tr><th align="left" id="d94826e113">

Scenario

</th><th align="left" id="d94826e116">

Steps

</th></tr></thead><tbody><tr><td id="d94826e122">

**Require approval**

</td><td>

On the **AI systems**, **MCP servers**, or **AI models** row, select **Activate**.

</td></tr><tr><td id="d94826e146">

**Stop requiring approval**

</td><td>

1.  On the asset type's row, select **Deactivate**.
2.  In the confirmation dialog box, select **Deactivate**.


</td></tr></tbody>
</table>    Without the requirement, assets of that type can be deployed without AI steward approval, but an AI asset manager can still request approval manually.

4.  In the **Automated requests** section, set whether approval requests are triggered automatically for AI assets.

<table><thead><tr><th align="left" id="d94826e188">

Scenario

</th><th align="left" id="d94826e191">

Steps

</th></tr></thead><tbody><tr><td id="d94826e197">

**Start approval requests automatically**

</td><td>

On the **Automatically trigger playbooks** row, select **Activate**.

</td></tr><tr><td id="d94826e215">

**Start approval requests manually**

</td><td>

1.  On the **Automatically trigger playbooks** row, select **Deactivate**.
2.  In the confirmation dialog box, select **Deactivate**.


</td></tr></tbody>
</table>    Starting approval requests automatically is recommended on production instances, so new AI assets don't wait for someone to request approval.


## Result

The **Status** column shows **Active** for each requirement you turned on and **Inactive** for each one you turned off.

**Parent Topic:**[Configuring builder controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-builder-controls.md)

