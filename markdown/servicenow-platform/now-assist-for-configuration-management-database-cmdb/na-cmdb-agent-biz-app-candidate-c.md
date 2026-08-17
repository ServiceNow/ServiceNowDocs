---
title: Business application candidate agent
description: The Business application candidate agent discovers and suggests business applications to associate with existing application services in the CMDB, reducing manual mapping effort and improving data governance. The agent uses AI clustering and feedback loops to propose business application candidates for your review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-biz-app-candidate-c.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 2
keywords: [business applications, app services, CMDB, AI automation, NowAssist, ServiceNow Otto for CMDB]
breadcrumb: [Using agentic workflows, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Business application candidate agent

The Business application candidate agent discovers and suggests business applications to associate with existing application services in the CMDB, reducing manual mapping effort and improving data governance. The agent uses AI clustering and feedback loops to propose business application candidates for your review.

**Important:**

Generative AI might produce inaccurate or incomplete information. Always validate AI-generated recommendations and accept or reject them based on your organization's governance policies.

## Required role

Access to all business application candidate agent tables, forms, and configuration requires the `sn_cmdb_admin` role.

## What is it

The agent uses existing service instance and user group data to infer business applications and to generate candidate records that admins can review and promote to actual records.

Business applications are logical representation of business functions. It is challenging to manually map hundreds of application services to business applications. The Business application candidate agent uses generative AI to automatically group related app services, infer the business applications they collectively represent, and surface these as reviewable recommendations. Each recommendation can be accepted or rejected — and rejections feed back into the AI to improve future results.

The agent surfaces application services that have no linked business application and proposes new business application records for your review and approval. The agent uses generative AI clustering, ServiceNow Otto skills, and continuous feedback from your rejection decisions to improve recommendation quality over time.

\[Omitted image "otto-biz-app-candidate-flow.png"\] Alt text: Example: Generating a candidate.

## Key benefits

The Business application candidate agent provides the following benefits:

-   Reduces manual effort required to map application services to business applications
-   Improves CMDB data quality and consistency through automated relationship discovery
-   Uses AI to identify patterns and relationships humans might miss
-   Learns and improves from human feedback on rejected recommendations

## How it works

The Business application candidate agent runs as two synchronized background jobs that manage data and generate recommendations:

Application Service Data Synchronization

The job copies app services and business applications into internal, AI-search-optimized tables where the AI engine can access them efficiently.

-   The job runs weekly by default, or more frequently during initial setup.
-   On the first run, the job bulk-loads all records; subsequent runs pick up only changed records.
-   The job completes before the Processing job begins generating recommendations.

The AI captures human acceptance and rejection decisions. Uses rejection decisions to refine its clustering and matching logic, improving future recommendations.

## System overview

The Business application candidate agent operates through the following system components:

-   **Scheduled Jobs:** Control whether the agent is active or deactivated.
-   **Work queues:** Track processing progress through the synchronization and recommendation stages.
-   **Run-state table:** Maintains statistics and configuration for each processing cycle.
-   **Recommendation table:** Stores recommendations for human review, acceptance, or rejection.

-   **[Review Business application candidate agent recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-biz-app-candidate-rec.md)**  
Review and evaluate the agent's recommendations to map application services to business applications. Accept a recommendation to create a business applications and relationships. Reject a recommendation to provide feedback that improves future recommendations.

**Parent Topic:**[Using agentic workflows in ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.md)

**Related topics**  


[Business application candidate agent reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-biz-app-candidate-ref.md)

