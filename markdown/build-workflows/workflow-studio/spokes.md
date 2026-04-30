---
title: Spokes
description: Add application-specific content to Workflow Studio by installing spokes.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Workflow Studio flow integrations, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Spokes

Add application-specific content to Workflow Studio by installing spokes.

A spoke is a scoped application containing Workflow Studio content dedicated to a particular application or record type. For example, the **ITSM Spoke** contains actions for managing Task records such as the **Create Task** action. Spokes are activated when their parent application is activated. For example, the **ITSM Spoke** is activated when the Incident, Problem, and Change applications are activated. Creating a spoke requires familiarity with application development as developers must add Workflow Studio content to a scoped application.

|Spoke|Description|Plugin|Included with|
|-----|-----------|------|-------------|
|[Benchmarks Spoke](../reference/benchmarks-actions.md)|Provides read-only actions for the read-only Benchmark Recommendation Evaluator flow.|\[com.sn\_bm\_client.spoke\]|[Benchmarks](https://www.servicenow.com/docs/access?context=r_Benchmarks&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) application.|
|[Connect spoke](../reference/connect-spoke.md)|Provides actions to automate the creation of conversations, to add users to a conversation, and to send messages to a conversation. These actions work with Connect API version 3 and later.|\[com.glide.connect\_v3plus.core.ah\]|ServiceNow AI Platform|
|[Customer Service Spoke](../reference/customer-service-actions.md)|Provides actions for flow designers to use when creating Customer Service Management business processes.|\[com.snc.customer\_service.spoke\]|[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) application|
|[External Related Files spoke](../reference/ext-related-files.md)|The External Related Files spoke stores information about files in third-party systems and helps you manage the information.|\[com.sn.external.files\]|ServiceNow AI Platform|
|[Field Service Spoke](../reference/field-service-actions.md)|Provides actions for flow designers to use when creating Field Service Management business processes.|\[com.snc.field\_service.spoke\]|[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US) application|
|[ITSM spoke](../reference/itsm-spoke.md)|Provides flow and actions associated with ITSM. Requires the ITSM application suite.|\[com.snc.itsm.spoke\]|[IT Service Management](https://www.servicenow.com/docs/access?context=r_ITServiceManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) application|
|[Machine Learning solutions for Flow Designer](../reference/predictive-intelligence-spoke.md)|Provides actions to make predictions from trained Predictive Intelligence solutions.|\[com.snc.ml\_flowdesigner\]|[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)|
|[Robotic Process Automation \(RPA\) Spoke](../reference/rpa-actions.md)|Provides RPA actions for flow designers to assign users to attended automation process, add work queue items to queue, update work items, fetch process jobs and execution status of a specific process job, trigger a specific bot process, and unassign users from attended automation process.|\[com.sn\_rpa\_foundation\]|[Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|
|[Security Operations spoke](../../integrationhub/reference/secops-spoke.md)|Provides Security Operations actions for flow designers to manage Security Incident Response flow templates.|\[com.snc.secops.spoke\]|[Security Operations](https://www.servicenow.com/docs/access?context=security-operations-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) application|
|[Visual Task Board \(VTB\) Spoke](../reference/vtb-actions.md)|Provides VTB actions for flow designers to manage the boards, lanes, cards, board members, and assignees.|\[com.glide.ui.vtb.ah\]|ServiceNow AI Platform|

Additional spokes are available with an Integration Hub subscription. To see a list of Integration Hub spokes, see [Integration Hub available\\n spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US). For more information about requesting an Integration Hub subscription, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

-   **[Benchmarks Spoke](../reference/benchmarks-actions.md)**  
Provides read-only actions for the read-only Benchmark Recommendation Evaluator flow.
-   **[Connect spoke](../reference/connect-spoke.md)**  
Provides actions to automate the creation of conversations, to add users to a conversation, and to send messages to a conversation. These actions work with Connect API version 3 and later.
-   **[Customer Service Spoke](../reference/customer-service-actions.md)**  
Provides actions for flow designers to use when creating Customer Service Management business processes. Requires the Customer Service Management \[com.sn\_customerservice\] plugin.
-   **[External Related Files spoke](../reference/ext-related-files.md)**  
The External Related Files spoke stores information about files in third-party systems and helps you manage the information.
-   **[Field Service Spoke](../reference/field-service-actions.md)**  
Provides actions for flow designers to use when creating Field Service Management business processes.
-   **[ITSM spoke](../reference/itsm-spoke.md)**  
Provides flow and actions associated with ITSM. Requires the ITSM application suite.
-   **[Machine Learning solutions for Flow Designer](../reference/predictive-intelligence-spoke.md)**  
With Predictive Intelligence for Flow Designer \(com.snc.ml\_flowdesigner\), you can deploy machine learning solutions in your instance. This spoke provides actions to incorporate Predictive Intelligence model predictions into flows.
-   **[Robotic Process Automation \(RPA\) Spoke](../reference/rpa-actions.md)**  
With Robotic Process Automation, your flow designers can use actions to assign and unassign users to and from an attended automation process, add work items to a queue, update work items, fetch process jobs, get the status of a process job, and trigger a bot process.
-   **[Security Operations spoke](../../integrationhub/reference/secops-spoke.md)**  
Provides Security Operations actions for flow designers to manage Security Incident Response flow templates.
-   **[Visual Task Board \(VTB\) Spoke](../reference/vtb-actions.md)**  
Provides VTB actions for flow designers to manage the boards, lanes, cards, board members, and assignees.

**Parent Topic:**[Workflow Studio flow integrations](flow-designer-integrations.md)

