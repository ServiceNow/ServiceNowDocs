---
title: Configure skill deployment settings
description: Configure the deployment settings for the skill that you have created. The deployment settings enable you to choose where the admin can find the skill in AI Admin Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/configure-skill-settings.html
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-04-17"
reading_time_minutes: 4
breadcrumb: [Configuring AI Skill Kit, AI Skill Kit, Enable AI experiences]
---

# Configure skill deployment settings

Configure the deployment settings for the skill that you have created. The deployment settings enable you to choose where the admin can find the skill in AI Admin Hub.

## Before you begin

Role required: sn\_skill\_builder.admin

## About this task

Deployment settings control two things: where the skill appears in the AI Admin Hub console for an admin, and which activation methods are available to that admin. You must configure both before publishing the skill.

**Important:** Deployment settings for cloned ServiceNow skills cannot be edited. If you select **Deployment settings** on a cloned skill, a notification informs you that these settings are locked. To use custom deployment settings, create a skill from scratch instead of cloning.

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select the skill that you want to configure from the **Custom Skills** list.

3.  Select the **4. Deployment and skill settings** tab.

4.  Select **Deployment Settings**.

5.  In the **ServiceNow Otto features** section, fill in the fields.

<table id="table_qfd_3nh_lcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workflow

</td><td>

The high-level category that this skill pertains to, such as **Technology**, **Employee**, **Creator**, or **Platform**. You can also select **Other** if none of the categories fit.

 The workflow that you choose determines where the skill appears in the AI Admin Hub console.

</td></tr><tr><td>

Product

</td><td>

The specific product that this skill operates within, such as ITSM, ITOM, HR Service Delivery, AI Admin Hub.

</td></tr><tr><td>

Feature

</td><td>

The feature that the skill is used on, such as Agent Chat, Knowledge, Virtual Agent. You can also define a custom feature if necessary.**Note:** If you select **Create new feature**, you're prompted for a name and description of the new feature.

</td></tr><tr><td>

Name

</td><td>

The name of the feature.

</td></tr><tr><td>

Description

</td><td>

A description of the feature.

</td></tr></tbody>
</table>6.  Select the check boxes for the deployment locations where you want the admin to be able to activate the skill.

<table id="table_deploy_locations"><thead><tr><th>

Location

</th><th>

Description

</th><th>

Additional Information

</th></tr></thead><tbody><tr><td>

ServiceNow Otto panel

</td><td>

Allows the skill to be triggered through the ServiceNow Otto Panel.

</td><td>

The ServiceNow Otto panel is the conversational interface found within the ServiceNow Otto Center, learn more about this feature at [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-center-now-assist-panel.md).

</td></tr><tr><td>

UI Action

</td><td>

Adds a UI action button to the core UI to trigger the skill. Once activated, the button appears on the table form specified during skill configuration.

</td><td>

After this option is selected, select a table, in the **Table** field, then select **Create UI Action**. After the skill has been created, select **Link to UI Action**.

 **Note:** The created UI Action is inactive by default.

 Learn more about UI Actions at [Defining UI actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_UIActions.md).

</td></tr><tr><td>

Flow action

</td><td>

Allows the skill to be used from a flow action. Once activated, you can access the skill through the **Execute Skill** flow action in Workflow Studio.

</td><td>

Details on the **Execute Skill** flow action can be found at [Execute Skill action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/execute-skill-action.md).

</td></tr><tr><td>

ServiceNow Otto context menu

</td><td>

Makes the skill available for activation and use through the ServiceNow Otto context menu.

</td><td>

For details on the context menu, see[ServiceNow Otto context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-write-overview.md).

</td></tr><tr><td>

Virtual assistants

</td><td>

Makes the skill available for activation and use in various chat experiences with virtual assistants.

</td><td>

For more information about ServiceNow Otto in Virtual Agent, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

UI Builder

</td><td>

Makes the skill available in UI Builder. You can find it in the Data and scripts panel.

</td><td>

Learn how to use UI Builder to create web user interfaces at [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md).

</td></tr></tbody>
</table>    **Tip:** You can select more than one deployment location. Selecting a location here makes it available for an admin to activate, but not activate the skill automatically. An admin must still activate the skill in AI Admin Hub. To learn more, see [Activate a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/activate-skill.md).

7.  Select **Save**.


## What to do next

After you configure the skill settings, you can publish your skill. To learn more about publishing skills, see [Finalize and publish a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/publish-skill.md).

**Parent Topic:**[Configuring AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/configuring-now-assist-skill-kit.md)

**Related topics**  


[Configure a skill prompt]()

[Configure security controls for a skill]()

