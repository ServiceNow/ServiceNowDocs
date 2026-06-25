---
title: Enterprise asset disposal order stages
description: An enterprise asset disposal order goes through various stages in the disposal process before it’s completed. With each stage, the task that's associated with that stage changes too.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/eamasset-disposalorder-stages.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Enterprise asset disposal order stages

An enterprise asset disposal order goes through various stages in the disposal process before it’s completed. With each stage, the task that's associated with that stage changes too.

Closing a task in the asset disposal process completes that task and automatically creates the next task in the process. For example, after you close the Schedule Pickup task, the state for that task changes to Closed Complete and the next task, Asset Departure, is created. This process continues until you close all the tasks required for disposing of the selected assets. After you close all the tasks, the disposal order is completed.

|Enterprise disposal stages|Task|Description|
|--------------------------|----|-----------|
|Draft|Verify Assets|Asset disposal record is created.|
|Scheduling|Schedule Pickup|Scheduling details for the asset disposal order.|
|Transit|Asset Departure|Verified assets are ready for departure.|
|Confirmation|Vendor Confirmation|Asset disposal order is confirmed by the vendor.|
|Documentation|Disposal Documentation|Documentation for the disposal record is attached.|
|Completed|None|Asset disposal record request is completed.|
|Cancelled|None|Disposal order can be canceled only until the transit stage.|

**Parent Topic:**[Enterprise Asset Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management]()

[Components installed with Enterprise Asset Management]()

[OT Asset Workspace roles]()

[Asset fields for enterprise assets]()

[Asset audit fields for enterprise assets]()

[Audit results]()

[Enterprise model categories and corresponding classes]()

[Mandatory fields in the bulk import spreadsheets]()

[Normalization status for enterprise models]()

[Model fields for Enterprise Asset Management]()

[Contract fields for Enterprise Asset Management]()

[Maintenance plan fields for Enterprise Asset Management]()

[Maintenance schedule fields for Enterprise Asset Management]()

[Work plan fields for Enterprise Asset Management]()

[Work plan schedule fields for Enterprise Asset Management]()

[Expense line fields for Enterprise Asset Management]()

[Fields inherited from a parent asset group to a sub group]()

[Terminology for linear assets]()

[Scheduled jobs and tables installed with normalization of firmware models]()

[Asset put away task fields]()

