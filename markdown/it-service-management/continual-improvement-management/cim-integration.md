---
title: Applications integrated with Continual Improvement Management
description: CIM provides integrations with other ServiceNow applications to enable you to create improvement initiatives from these applications. You can also create records for integrated applications from improvement initiatives.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/continual-improvement-management/cim-integration.html
release: zurich
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Overview, Continual Improvement Management, IT Service Management]
---

# Applications integrated with Continual Improvement Management

CIM provides integrations with other ServiceNow® applications to enable you to create improvement initiatives from these applications. You can also create records for integrated applications from improvement initiatives.

You can link multiple tasks from integrated applications to a single CIM task and link multiple CIM tasks to a single integrated application task.

## Applications from which you can create Improvement Initiatives

-   [Benchmarks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/benchmarks/benchmarks-landing.md)
-   [Coaching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/coaching/cf-coaching-landing.md)
-   
-   Customer Service Management
-   Demand Management
-   Governance, Risk, and Compliance \(GRC\)
-   Idea Portal
-   [Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/c_IncidentManagement.md)
-   [Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/c_ProblemManagement.md)
-   
-   Survey Management
-   [Vendor Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/vendor-management-workspace/vendor-management-workspace-landing-page.md)

For more information, see [Create improvement initiatives from integrated applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/continual-improvement-management/create-improvmt-from-apps.md).

## Application records you can create from improvement initiatives

-   Change record \([Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/c_ITILChangeManagement.md)\)
-   Coaching opportunity \([Coaching opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/coaching/cf-create-coaching-opportunity.md)\)
-   Knowledge base article \(\)
-   Demand record \(Demand Management\)
-   Project \(Project Management\)
-   Story record \(\)

For more information, see [Create application records from improvement initiatives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/continual-improvement-management/create-app-records.md).

## Summary of CIM Integration with other applications

|Application|Application record|Create improvement initiative|Create application record from improvement initiative|
|-----------|------------------|-----------------------------|-----------------------------------------------------|
|GRC|
|Audit Management|Issue record|X|--|
|Strategic Portfolio Management|
|Agile Development|Story record|--|X|
|Demand Management|Demand record|X|X|
|Project Management|Project record|--|X|
|IT Operations Management|
|CMDB|Remediate Duplicate Task record|X|--|
|IT Service Management|
|Benchmarks|Benchmarks recommendation|X|--|
|Change Management|Change record|--|X|
|Major Incident Management|Post incident review workbench|X|--|
|Problem Management|Problem record|X|--|
|Platform Capabilities|
|Knowledge Management|Knowledge base article|--|X|
|Survey Management|Survey|X|--|
|Service Management|
|Coaching|Coaching opportunity|X|X|

-   **[Create improvement initiatives from integrated applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/continual-improvement-management/create-improvmt-from-apps.md)**  
Create improvement initiatives from applications integrated with Continual Improvement Management to enable planning, implementation, monitoring, and impact assessment of improvements in a centralized framework.
-   **[Create application records from improvement initiatives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/continual-improvement-management/create-app-records.md)**  
Create records for integrated applications from improvement initiatives or CIM tasks to transform improvement initiatives into broader, actionable efforts to enable improvements across teams and processes.
-   **[Configure CIM integration property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/continual-improvement-management/configure-cim-int-property.md)**  
Configure the CIM sn\_cim.initiative\_copy\_attributes integration property to define field values to be copied from an improvement initiative to application records that you create from the initiative.

**Parent Topic:**[Continual Improvement Management overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/continual-improvement-management/get-started-cim.md)

**Related topics**  


[bundle-crapiref.extension-points]

[bundle-crapiref.scripted-extension-points]

[bundle-crapiref.ui-extension-points]

[bundle-crapiref.client-extension-points]

