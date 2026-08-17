---
title: Robotic Process Automation \(RPA\) bot generation skill
description: Use the RPA bot generation skill to create automations, activities, and automation logic additions from text instructions and preview options from the RPA Desktop Design Studio user interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/rpa-bot-generation.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2026-07-31"
reading_time_minutes: 4
keywords: [Now Assist, generative AI]
breadcrumb: [AI in RPA Hub, Explore, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Robotic Process Automation \(RPA\) bot generation skill

Use the RPA bot generation skill to create automations, activities, and automation logic additions from text instructions and preview options from the RPA Desktop Design Studio user interface.

The skill enables citizen developers to participate in the automation development process. Citizen developers can contribute their domain expertise and knowledge of business processes to create automation flows. A citizen developer can quickly and easily create automation flows by describing the task or process in natural language via text. No in-depth technical knowledge of Robotic Process Automation \(RPA tools\) or programming languages is needed, which makes automation accessible to a wider audience.

The RPA bot generation skill streamlines the process of creating workflows, reducing the time and effort required to implement RPA solutions. An automation flow can be generated in minutes rather than hours or days, accelerating the time-to-value.

By generating automation flows through text-based descriptions, RPA becomes more approachable for individuals and businesses who may not have prior experience with automation or coding.

Access the RPA bot generation skill from the RPA Desktop Design Studio user interface.

Enable RPA bot generation to gain the following benefits:

-   Build simple, brand-new automations quickly and efficiently.
-   Easily add new activities to existing automations, ensuring modularity and scalability.
-   Use in-line prompting to refine automation logic, whether starting from components or a empty design surface.

## Roles

RPA developer \(sn\_rpa\_fdn.rpa\_developer\) or RPA admin \(sn\_rpa\_fdn.rpa\_admin\) roles are required to use this skill. These roles contain the AI Admin Hub user role \(sn\_nowassist\_admin.user\).

## Activation

Install the ServiceNow Otto for RPA Hub application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website. For more information, see [Install ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-now-assist-rpa-hub.md).

Then, turn on the RPA bot generation skill to use generative AI for creating automations and activities, and extending automation logic. For more information, see [Turn on the RPA bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/turn-rpa-bot-generation-skill.md).

You must have a subscription for ServiceNow Otto for Creator and RPA Hub applications.

## Limitations of the RPA bot generation skill

For more information about the limitations of the Robotic Process Automation \(RPA\) bot generation skill, see [Limitations of ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/limitations-rpa-bot-gen-skill.md).

## Accessing the generative AI capability in RPA Desktop Design Studio

If you log in to the RPA Desktop Design Studio with either RPA Developer or RPA Admin after enabling the RPA bot generation skill, the generative AI capability is available. In this scenario, you can create and edit automations, activities, and extend automation logic flow through text instructions and preview options.

If you log in to the RPA Desktop Design Studio with a role other than RPA Developer or RPA Admin after enabling the RPA bot generation skill, the generative AI capability will not be available. In this scenario, you will not be able to create and edit automations, activities, or extend automation logic flow through text instructions and preview options.

If you log in to the RPA Desktop Design Studio with a role other than RPA Developer or RPA Admin and then switch to one of these roles, you won't be able to access the generative AI capability. Restart the RPA Desktop Design Studio and log in with RPA Admin or Developer.

If you log in to the RPA Desktop Design Studio with either RPA Developer or RPA Admin, and then switch to any other user roles apart from these, you will encounter an error message when attempting to access the generative AI capability.

**Related topics**  


[Turn on the RPA bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/turn-rpa-bot-generation-skill.md)

[Create an automation with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-automation-now-assist.md)

[Create an activity with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-activity-now-assist.md)

[Build an automation with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/build-automation-now-assist.md)

[Example instructions for ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/example-instructions-rpa.md)

[Limitations of ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/limitations-rpa-bot-gen-skill.md)

