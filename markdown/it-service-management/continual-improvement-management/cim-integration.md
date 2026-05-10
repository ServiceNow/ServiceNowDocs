---
title: Applications integrated with Continual Improvement Management
description: CIM provides integrations with other ServiceNow applications to enable you to create improvement initiatives from these applications. You can also create records for integrated applications from improvement initiatives.
locale: en-US
release: australia
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Overview, Continual Improvement Management, IT Service Management]
---

# Applications integrated with Continual Improvement Management

CIM provides integrations with other ServiceNow® applications to enable you to create improvement initiatives from these applications. You can also create records for integrated applications from improvement initiatives.

You can link multiple tasks from integrated applications to a single CIM task and link multiple CIM tasks to a single integrated application task.

## Applications from which you can create Improvement Initiatives

-   [Benchmarks](../../benchmarks/reference/r_Benchmarks.md)
-   [Coaching](../../cf-coaching/reference/cf-coaching-landing.md)
-   [Configuration Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/manage-cmdb.md)
-   [Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md)
-   [Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-management/c_DemandManagement.md)
-   [Governance, Risk, and Compliance \(GRC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/r_WhatIsGRC.md)
-   [Idea Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/innovation-management/idea-portal.md)
-   [Incident Management](../../incident-management/concept/c_IncidentManagement.md)
-   [Problem Management](../../problem-management/concept/c_ProblemManagement.md)
-   [Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/process-mining.md)
-   [Survey Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_SurveyManagementLandingPage.md)

For more information, see [Create improvement initiatives from integrated applications](../task/create-improvmt-from-apps.md).

## Application records you can create from improvement initiatives

-   Change record \([Change Management](../../change-management/concept/c_ITILChangeManagement.md)\)
-   Coaching opportunity \([Coaching opportunity](../../cf-coaching/task/cf-create-coaching-opportunity.md)\)
-   Knowledge base article \([Create a knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/create-knowledge-article.md)\)
-   Demand record \([Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-management/c_DemandManagement.md)\)
-   Project \([Project Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_ProjectApplicationOverview.md)\)
-   Story record \([Agile Development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-development/agile-development.md)\)

For more information, see [Create application records from improvement initiatives](../task/create-app-records.md).

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

-   **[Integrate Continual Improvement Management using extension point](../task/integrate-extension-api.md)**  
Integrate CIM with other applications by using the CIMIntegrationAPI extension point. It defines the inbound and outbound extension points for integrating CIM with other applications.

**Parent Topic:**[Continual Improvement Management overview](../concept/get-started-cim.md)

**Related topics**  


[Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md)

[Using scripted extension points in server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/scripted-extension-points.md)

[Using UI extension points in server-side UI macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/ui-extension-points.md)

[Using client extension points in client-side UI scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/client-extension-points.md)

