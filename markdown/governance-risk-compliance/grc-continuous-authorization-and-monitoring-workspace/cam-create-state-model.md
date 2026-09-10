---
title: GRC state model configuration
description: Create a Governance, Risk, and Compliance state model to define the steps, transitions, and validations for a custom workflow in CAM. State models control how authorization packages move through workflow life cycles and determine which actions are available at each step.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-create-state-model.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CAM workflow configuration, Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# GRC state model configuration

Create a Governance, Risk, and Compliance state model to define the steps, transitions, and validations for a custom workflow in CAM. State models control how authorization packages move through workflow life cycles and determine which actions are available at each step.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **GRC State Models**.

2.  Select **New** to create a state model record.

3.  On the **GRC state model New record** form, fill in the fields.

    |Fields|Descriptions|
    |------|------------|
    |Name|Enter a name for the state model.|
    |Active|Select the **Active** option to enable the state model.|
    |Table name|Select **Authorization Package \[sn\_irm\_cont\_auth\_auth\_pack\]**.|
    |State field|Select **State Model \[state\_model\]**.|
    |State model|Select **Step \[step\]**.|

4.  Select **Submit**.

    You’re directed to the **GRC state models** list page.


## Result

The state model is ready to be configured with workflow states, transitions, and attributes. After completing the configuration, you can map the state model to a workflow configuration and use it for authorization packages.

## What to do next

[Create GRC workflow states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/add-workflow-states.md)

[Add existing attributes to a GRC workflow state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/configure-state-model-attributes.md)

[Create a new state model attribute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/configure-new-state-model-attributes.md)

-   **[Create GRC workflow states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/add-workflow-states.md)**  
Add Governance, Risk, and Compliance workflow states to a state model to define the individual steps in your workflow. Each workflow state represents a phase in the authorization package life cycle and determines what you can do at that stage.
-   **[Add existing attributes to a GRC workflow state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/configure-state-model-attributes.md)**  
Add existing Governance, Risk, and Compliance state model attributes to add special capabilities to workflow steps without custom code. Attributes control features like approval requirements, report generation, and Open Security Controls Assessment Language \(OSCAL\) file exports for specific workflow states.
-   **[Create a new state model attribute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/configure-new-state-model-attributes.md)**  
Create custom state model attributes to add specialized capabilities to workflow steps.

**Parent Topic:**[CAM workflow configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-workflow-configurator.md)

