---
title: Project eligibility analysis AI agent
description: This Strategic Portfolio Management agent performs checks for project and project task related requests. The agent analyzes requests to check impact on a project due to project task. It checks if the project summary email skill is enabled for the instance and whether the skill was enabled for a given project.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/spm-project-eligibility-analysis-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Strategic Portfolio Management AI agents, Strategic Portfolio Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Project eligibility analysis AI agent

This Strategic Portfolio Management agent performs checks for project and project task related requests. The agent analyzes requests to check impact on a project due to project task. It checks if the project summary email skill is enabled for the instance and whether the skill was enabled for a given project.

## Workflow

1.  Verify that the project summary email skill is enabled on the instance.
2.  Retrieve the parent project information using the input task number.
3.  Verify that the project manager has scheduled a project summary email for this project.
4.  If both checks pass, hand off to the next agent to analyze the task's impact on the project. If either check fails, terminate the workflow.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Flow Action**

Check if project email insights skill is enabled

-   **Scripts**

Fetch Email insight configuration and check if critical update

Get project details for a given task number


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

project\_manager

</td></tr><tr><td>

Data access roles

</td><td>

agent\_role\_config\_viewer, agent\_workspace\_user, app\_service\_user, baseline\_user, canvas\_user, cmdb\_ms\_user, cmdb\_query\_builder, cmdb\_query\_builder\_read, cmdb\_read, currency\_instance\_report\_admin, data\_manager\_user, decision\_table\_reader, demand\_manager, demand\_user, dependency\_views, financial\_mgmt\_user, fiscal\_calendar\_user, idea\_manager, interaction\_agent, it\_demand\_manager, it\_demand\_user, it\_project\_manager, it\_project\_portfolio\_user, it\_project\_user, notify\_view, now\_assist\_panel\_user, pa\_viewer, planning\_console\_user, pps\_resource, project\_manager, project\_portfolio\_user, project\_user, prompt\_library\_user, rate\_model\_user, report\_group, report\_user, resource\_user, rm\_doc\_admin, rm\_epic\_admin, rm\_release\_scrum\_admin, rm\_scrum\_task\_admin, rm\_sprint\_admin, rm\_story\_admin, rm\_task\_admin, rm\_test\_admin, role\_viewer, scrum\_admin, scrum\_user, skill\_user, snc\_internal, snc\_required\_script\_writer\_permission, sn\_ace.ace\_user, sn\_ai\_filter\_assist.user, sn\_ai\_filter\_tracker.user, sn\_bm\_client.benchmark\_data\_viewer, sn\_change\_read, sn\_cmdb\_user, sn\_csm\_household.viewer, sn\_csm\_pricing.pricelist\_viewer, sn\_customerservice.customer\_data\_viewer, sn\_gf.goal\_user, sn\_gf.goal\_user\_read, sn\_gf.strategy\_planner, sn\_gf.strategy\_planner\_read, sn\_ind\_tmt\_orm.fulfillment\_viewer, sn\_ind\_tmt\_orm.order\_viewer, sn\_invst\_pln.std\_user, sn\_invst\_pln\_investment\_user, sn\_invst\_pln\_v2.investment\_user, sn\_l2c\_core.entity\_mapping\_viewer, sn\_nowassist\_admin.user, sn\_ord\_qual\_mgmt.alternate\_proposal\_read, sn\_prd\_invt.product\_inventory\_operations\_read, sn\_prd\_invt.product\_inventory\_viewer, sn\_prd\_pm.characteristics\_viewer, sn\_prd\_pm.product\_catalog\_viewer, sn\_prd\_pm.product\_model\_characteristic\_viewer, sn\_pss\_core.service\_contract\_viewer, sn\_query\_gen.user, sn\_shn.user, sn\_sow.sow\_home, sn\_sow.sow\_list, sn\_sow.sow\_user, sn\_spm\_gen\_ai.assist\_user, sn\_sttrm\_condition\_read, sn\_tmt\_core.inbound\_queue\_read, sn\_udc.basic\_read, sn\_uib\_collab.user, sn\_workflow\_studio.workflow\_studio\_read, survey\_reader, task\_editor, template\_read\_global, timecard\_approver, timecard\_user, timeline\_user, view\_changer, viz\_creator, workspace\_user

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Generate Project Summary

</td></tr></tbody>
</table>Learn more about Strategic Portfolio Management at [Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/r_ITBusinessManagement.md).

**Parent Topic:**[Strategic Portfolio Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/spm-ai-agents-overview.md)

