---
title: Viewing templates associated with an AI system
description: Learn how value is being measured for an AI system by viewing the value templates mapped to the asset and the productivity calculation each template uses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/measuring-ai-asset-value-templates.html
release: zurich
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [value templates, AI system templates, productivity calculation, template mapping, mapping status]
breadcrumb: [Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Viewing templates associated with an AI system

Learn how value is being measured for an AI system by viewing the value templates mapped to the asset and the productivity calculation each template uses.

Value templates define the formula used to calculate productivity gains for an AI system. The formula multiplies a usage metric by a time constant and a quality constant to produce a minutes-saved figure. Because each AI system can have templates mapped to different personas, the **Templates** tab gives you a per-asset view of exactly which templates are active and what each one calculates.

## Value templates list

The **Templates** tab displays a **Value templates** section that lists all templates mapped to the AI system. Each template card shows the following attributes.

|Attribute|Description|
|---------|-----------|
|Template name|Name of the value template mapped to this AI system.|
|Mapping status|Publication state of the template mapping. A **Published** mapping is active and contributes to value calculations. A **Retired** mapping is no longer used in calculations but remains visible for historical reference.|
|Persona|User role for whom the productivity value is calculated.|
|Department|Department associated with the template mapping, if specified.|
|Category|Value template category, such as Productivity.|
|Usage|Usage indicator that supplies the daily invocation count used in the productivity formula.|
|Time|Time constant \(in minutes\) applied per invocation in the productivity formula.|
|Quality|Quality constant \(as a percentage\) applied in the productivity formula. Represents the expected acceptance rate of AI outputs.|

By default, only templates with an active mapping status are shown. To include retired templates in the list, enable the **Include retired templates** toggle.

## Template details side panel

To review the full configuration of a template mapping, select **View details** on a template card. A side panel opens showing the following information.

|Field|Description|
|-----|-----------|
|**Mapped template**|Name of the value template mapped to this AI system.|
|**Mapping status**|Publication state of this template mapping.|
|**Persona**|User role for whom value is calculated using this template.|
|**Productivity gained**|Total minutes saved by this persona using this AI system over the selected time period, shown as a trend chart. Use the date range selector to adjust the reporting window.|
|**Productivity calculation using this template**|The formula applied to calculate productivity for this mapping, expressed as: Usage indicator × time constant \(minutes\) × quality constant \(%\). Select the usage indicator link to open its record.|

To view the full template record and its configuration fields, select **Open template** in the **Template details** section of the side panel.

**Parent Topic:**[Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-managing-ai-assets.md)

