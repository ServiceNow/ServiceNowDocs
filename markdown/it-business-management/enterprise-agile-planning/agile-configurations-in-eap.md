---
title: Agile configurations in EAP
description: Learn about the different SAFe configurations available in Enterprise Agile Planning \(EAP\) so that you can work with your admin to update the configuration according to your team's needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/enterprise-agile-planning/agile-configurations-in-eap.html
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Agile configurations in EAP

Learn about the different SAFe configurations available in Enterprise Agile Planning \(EAP\) so that you can work with your admin to update the configuration according to your team's needs.

## Default EAP configurations

A configuration includes the team level structure and work item types. The following Agile configurations, with the relevant team level, work item type, and planning calendar mapping, are available by default:

-   Full Configuration
-   Essential Configuration
-   Large Solution Configuration
-   Portfolio Configuration
-   Kanban Configuration

\[Omitted image "eap-configurations.png"\] Alt text: Default EAP configurations in the Strategic Planning Workspace.

If you installed the Strategic Planning demo data, **Full Configuration** is activated for you. You can choose to activate a different configuration or define a new configuration.

For more information, see [Activate an EAP configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/activate-eap-configuration.md) or [Create or update a configuration in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/create-eap-configuration.md).

## Default team level and work item hierarchy

\[Omitted image "eap-team-work-item-hiearachy.png"\] Alt text: Team level hierarchy and work item type roll up for EAP configuration in the Strategic Planning Workspace.

-   The EAP teams follow the hierarchy of Portfolio &gt; Solution Train &gt; Agile Release Train &gt; Agile Team.
-   The work item types follow the hierarchy of Epic &gt; Capability &gt; Feature &gt; Story.

    However, while setting up a new configuration or editing an existing configuration, you can assign any work item type to any team level. For example, a Feature can be mapped to the Solution Train level or a Story can be mapped to the ART level. Based on how teams in your organization choose to operate, you can flexibly define or update the EAP configurations.

-   All work items types used in EAP extend from the EAP Planning item \[sn\_align\_core\_eap\_planning\_item\] table, which in turn extends from the Planning Item \[sn\_align\_core\_planning\_item\] table of Strategic Planning.
-   The Story records are saved in the Story \[rm\_story\] table.

    You can also create a custom work item type. See [Create a custom work item type in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/create-custom-work-item-type-in-eap.md).


