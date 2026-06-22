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
-   [Configuration Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/configuration-management-database-cmdb/manage-cmdb.md)
-   [Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/c_CustomerServiceManagement.md)
-   [Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/demand-management/c_DemandManagement.md)
-   [Governance, Risk, and Compliance \(GRC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/governance-risk-and-compliance/r_WhatIsGRC.md)
-   [Idea Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/innovation-management/idea-portal.md)
-   [Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/c_IncidentManagement.md)
-   [Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/c_ProblemManagement.md)
-   [Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/process-mining/process-mining.md)
-   [Survey Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/ai-platform-capabilities/r_SurveyManagementLandingPage.md)
-   [Vendor Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/vendor-management-workspace/vendor-management-workspace-landing-page.md)

For more information, see [Create improvement initiatives from integrated applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/continual-improvement-management/create-improvmt-from-apps.md).

## Application records you can create from improvement initiatives

-   Change record \([Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/c_ITILChangeManagement.md)\)
-   Coaching opportunity \([Coaching opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/coaching/cf-create-coaching-opportunity.md)\)
-   Knowledge base article \([Create a knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-management/create-knowledge-article.md)\)
-   Demand record \([Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/demand-management/c_DemandManagement.md)\)
-   Project \([Project Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/project-management/c_ProjectApplicationOverview.md)\)
-   Story record \([Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/agile-development/agile-landing-page.md)\)

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


[Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/web-services/extension-points.md)

[Using scripted extension points in server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/web-services/scripted-extension-points.md)

[Using UI extension points in server-side UI macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/web-services/ui-extension-points.md)

[Using client extension points in client-side UI scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/web-services/client-extension-points.md)

