---
title: Workday external content connector
description: The Workday external content connector retrieves help articles, benefits, learning assignments, Manager Insights Hub data, payroll information, PTO information, and vacation policies from your Workday source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Workday external content connector

The Workday external content connector retrieves help articles, benefits, learning assignments, Manager Insights Hub data, payroll information, PTO information, and vacation policies from your Workday source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure Workday security settings](../task/configure-workday-security-settings.md)**  
Create an unconstrained integration system security group in Workday. The Workday external content connector uses this security group when accessing your Workday content.
-   **[Configure access to help articles in Workday](../task/configure-public-help-articles-workday.md)**  
Create an article audience rule in Workday and specify it for your help articles to make them accessible by all your employees. The Workday external content connector uses the audience rule and article settings to make content and metadata from your help articles searchable.
-   **[Configure a payslip report in Workday](../task/configure-payslip-report-workday.md)**  
Configure a custom report for payroll data in Workday. The Workday external content connector uses this report to make content and metadata from your payroll data searchable.
-   **[Configure a Learning assignment custom report in Workday](../task/configure-learning-assignment-report-workday.md)**  
Configure a custom report for Learning assignments in Workday. The Workday external content connector uses this custom report to make content and metadata from your Learning assignment data searchable.
-   **[Get Workday task code for Find Learning Assignments](../task/get-workday-task-code-learning-assignments.md)**  
Get the task code for the Find Learning Assignments task from your Workday tenant. The Workday external content connector needs this task code to retrieve Learning assignment data from Workday.
-   **[Get Workday task code for My Team's Birthday](../task/get-workday-task-code-birthday.md)**  
Get the task code for the My Team's Birthday task from your Workday tenant. The Workday external content connector needs this task code to retrieve team birthday data from the Manager hub.
-   **[Get Workday task code for My Team Anniversaries](../task/get-workday-task-code-anniversaries.md)**  
Get the task code for the My Team Anniversaries task from your Workday tenant. The Workday external content connector needs this task code to retrieve team anniversary data from the Manager hub.
-   **[Configure Workday for external content indexing](../task/configure-workday-external-content-indexing.md)**  
Create and authorize an OAuth 2.0 API client in your Workday tenant to allow the Workday external content connector to access your Workday source system.
-   **[Create a Workday external content connector](../task/create-ext-cont-connector-workday.md)**  
Create an external content connector to retrieve searchable content from your Workday source system.
-   **[Configure crawl settings for a Workday external content connector](../task/configure-crawl-settings-workday-external-content-connector.md)**  
Specify the content types you want your Workday external content connector to retrieve.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

