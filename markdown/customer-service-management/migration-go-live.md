---
title: Go live with CSM Configurable Workspace
description: After you complete the migration steps, prepare your agents and your instance for go-live. A phased rollout gives you time to catch configuration gaps before all agents switch over.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/migration-go-live.html
release: zurich
topic_type: concept
last_updated: "2026-11-13"
reading_time_minutes: 3
breadcrumb: [Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Go live with CSM Configurable Workspace

After you complete the migration steps, prepare your agents and your instance for go-live. A phased rollout gives you time to catch configuration gaps before all agents switch over.

## Keep store apps updated

CSM Configurable Workspace is delivered as a store app with quarterly updates. Keeping the app updated gives agents the latest capabilities and makes upgrades go smoothly. Before go-live, verify that you're on the latest version of the store app.

## Pilot with a smaller agent group

CSM Configurable Workspace and CSM Agent Workspace can run on the same instance at the same time. Before you switch all agents over, pilot the new workspace with a smaller group of agents who are willing to give feedback and who represent the typical workflows in your organization.

During the pilot, track the metrics you defined in your [migration goals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-plan.md), such as case creation time or the number of steps to close a case. Use the data to identify configuration gaps before a broader rollout.

## Involve agents throughout the process

Involve agents or team leads when you review the pilot results. Give agents a structured way to report issues with the new workspace and a clear process for how those issues are addressed.

Don't reproduce CSM Agent Workspace exactly as it was. Use the migration as an opportunity to remove friction from agent workflows, and plan three or four improvements to your workspace design that address known pain points.

## Provide structured training before go-live

CSM Configurable Workspace is a different working environment from CSM Agent Workspace, and agents need time to learn the interface before they work at full capacity. Plan for the following:

-   Identify workspace champions in each agent team. Champions learn the new workspace during the pilot and support their colleagues during the broader rollout.
-   Provide structured training sessions before go-live, with consistent communication about the change.
-   Reassure agents that there's an active process to monitor their feedback and act on it after go-live.
-   Plan staffing for the first weeks after agents switch over, and allow extra time for agents to reach their usual pace.

## Continue to iterate after go-live

After agents go live, create a roadmap for further improvements based on their feedback, and communicate progress regularly so that agents see their input lead to changes. Conduct an early post-go-live review to catch configuration gaps.

Track feature adoption to understand which workspace capabilities agents use and which they don't, and use this information to guide further configuration work.

## Learning resources for UI Builder

CSM Configurable Workspace is configured through UI Builder. Staying as close to the base system configuration as possible reduces upgrade effort and lets you benefit from new enhancements. If your team is new to UI Builder, the following resources can help:

-   [How do I learn UI Builder?](https://www.servicenow.com/community/next-experience-articles/how-do-i-learn-ui-builder-fundamentals-now-learning-course-free/ta-p/3130073) \(Next Experience and UI Builder community resources\)
-   [UI Builder Fundamentals](https://sn.works/UIBFunX)
-   Workshops and lab guides: [Next Experience workshops](https://sn.works/NEWorkshops), [Introduction to UI Builder lab guide](https://sn.works/K24IntroUIBLab), and [Advanced UI Builder lab guide](https://sn.works/K24AdvUIBLab)
-   [Next Experience Center of Excellence](https://nxtxp.link/coe)
-   [Next Experience Academy](https://sn.works/nextacademy)
-   [You and I Builder Live playlist](https://www.youtube.com/playlist?list=PL3rNcyAiDYK2Bgzj4mRdtfxMpGkI5KXBJ)

## Configure new capabilities after go-live

CSM Configurable Workspace includes capabilities that weren't available in CSM Agent Workspace. These aren't migration steps. Configure them after your agents are live in the new workspace.

|Capability|Description|More information|
|----------|-----------|----------------|
|Branding and theming|Apply your organization's colors and logo to the workspace using Theme Builder. You can create multiple themes and set a default, and agents can choose their preferred theme from the available options.|[Branding and theming](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-branding-theming.md)|
|AI Search and Genius Results|AI Search gives agents contextual search results in the Recommended Actions panel, and Genius Results displays the most relevant answer at the top of the search results. Agent Assist configuration carries over, but AI Search is a separate capability that you enable and configure. To check whether AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Recommended Actions is the default on the Front-line case page and the chat interaction page. To make Genius Results available, link a Genius Results configuration to your search profile.|[Using AI Search with CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-config-workspace-ai-search.md)|
|Collaborate|The Collaborate component lets agents start chats or meetings with colleagues, experts, or customers from a case record without leaving the workspace. Before you configure it, integrate the communication tool, such as Microsoft Teams or Zoom, with your instance.||

