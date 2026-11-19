---
title: ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) configuration prerequisites
description: Review these prerequisites before configuring skills or agentic workflows in any ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) application. Completing this checklist confirms that the required plugins are installed, roles are in place, and you are familiar with the shared activation procedures.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-tmt-checklist.html
release: brazil
topic_type: concept
last_updated: "2026-09-27"
reading_time_minutes: 1
breadcrumb: [ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\), Telecommunications, Media, and Technology \(TMT\)]
---

# ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) configuration prerequisites

Review these prerequisites before configuring skills or agentic workflows in any ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) application. Completing this checklist confirms that the required plugins are installed, roles are in place, and you are familiar with the shared activation procedures.

## Configuration prerequisites checklist

Before you activate a skill or agentic workflow in any TMT application, confirm the following prerequisites. Skill activation and workflow cloning work the same way for every ServiceNow Otto application.

-   The shared ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) plugin \(`sn_tmt_gen_ai`\) is installed, along with any additional plugin the specific application requires. See [Install ServiceNow Otto for TMT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/now-assist-tmt-install-all.md).

    **Note:** For instructions on installing ServiceNow Otto for Sales CRM for Telecommunications, see [Install ServiceNow Otto for Sales CRM for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/now-assist-tmt-install.md).

-   You have the admin role required to configure skills in the AI Admin Hub or AI Skill Kit.
-   \(Optional\) The ServiceNow Otto panel is activated, if you plan to expose skills there. See [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-now-assist-panel.md).
-   You're familiar with the general skill activation procedure — select a workflow group, activate and configure inputs, set availability and display, then activate. See [Activate an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-a-now-assist-skill.md).
-   You're familiar with the input data and prompt customization sub-steps, which are the same for every TMT application. See [Customize skill inputs and the prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/now-assist-tmt-customize-skill-inputs.md).
-   If you plan to customize an agentic workflow, you've duplicated it first — base system workflows are read-only. See [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md).
-   If you plan to clone and edit a skill's prompt directly, instead of through the AI Admin Hub, you're familiar with AI Skill Kit. See [Clone and edit a ServiceNow skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-and-edit-servicenow-skill.md).

