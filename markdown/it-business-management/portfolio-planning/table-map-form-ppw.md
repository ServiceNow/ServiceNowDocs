---
title: Table map form
description: Understand the fields of the table map form. This form is used to create a new custom table map for any record to integrate with Agile Development 2.0, SAFe, and PPM.
locale: en-US
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Form field information for Portfolio Planning, Reference, Portfolio Planning, Strategic Portfolio Management]
---

# Table map form

Understand the fields of the table map form. This form is used to create a new custom table map for any record to integrate with Agile Development 2.0, SAFe, and PPM.

|Field|Description|
|-----|-----------|
|Alignment Integration|Specifies the Alignment integration type. The value is **ServiceNow Internal** by default.|
|Execution table|Table in Agile Development 2.0, SAFe, or PPM that needs to be mapped with a table in Strategic Planning. For example, Defect \[rm\_defect\].|
|Alignment table|Table in Strategic Planning that needs to be mapped with a table in Agile Development 2.0, SAFe, or PPM. For example, Milestone \[sn\_milestones\_milestone\].|
|Milestone table map|This field is relevant only for Project \[pm\_project\] table map. It is a reference to the new Milestone table map \(sn\_milestones\_milestone\) for integrating project milestones from Project Portfolio Management workspace to Strategic Planning. For all the other table maps, the milestone table map field is not available.|
|Execution table filter|Filter condition to retrieve the relevant records from PPM, Agile Development 2.0, or SAFe. For example, Portfolio is HR or Active is True.​|
|Alignment table filter|Filter condition to retrieve the relevant records from Strategic Planning.​|
|Active flag|Ensures that the table map sync is active. This field is checked by default.|
|Sync attachments|Ensures that the attachments are synced between the applications. This field is checked by default.|

**Parent Topic:**[Form field information for Portfolio Planning](../../portfolio-planning/reference/form-field-information-for-portfolio-planning.md)

