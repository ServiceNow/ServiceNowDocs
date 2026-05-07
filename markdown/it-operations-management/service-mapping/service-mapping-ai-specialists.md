---
title: AI Agents for Service Mapping
description: AI Agents for Service Mapping are autonomous AI agents that automate the creation and maintenance of service maps in the Configuration Management Database \(CMDB\), reducing manual effort for Service Mapping administrators.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-04-16"
reading_time_minutes: 5
keywords: [AI Agent, Service Mapping, agentic AI, service map, CMDB, Business App Mapping, ML candidate]
breadcrumb: [AI capabilities in Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# AI Agents for Service Mapping

AI Agents for Service Mapping are autonomous AI agents that automate the creation and maintenance of service maps in the Configuration Management Database \(CMDB\), reducing manual effort for Service Mapping administrators.

AI agents for Service Mapping include two AI Agents that automate key parts of the service mapping workflow. After activation, both agents run autonomously in the background on a recurring schedule, processing all relevant records without requiring administrator input for each one.

## Available AI Agents

The ITOM AI Agents for Service Mapping application \[sn\_sm\_gen\_ai\] provides two AI Agents:

-   **Service Mapping AI Agent**

    Automatically creates ML-based service maps from Application Service Candidates \(ASCs\) and persists the full service topology in the CMDB. This Agent evaluates ML-powered candidates, focuses on those with a high-confidence name suggestion source such as Service Fingerprints \(SFPs\), filters out noise \(such as monitoring clients, security clients, and operating system processes\), and creates the service topology. Created service maps are set to non-operational by default so that the Service Mapping administrator can review them before making them operational.

-   **Business App Mapping AI Agent**

    Automatically creates Common Service Data Model \(CSDM\) "Uses::Used by" relationships between Business Applications \[cmdb\_ci\_business\_app\] and discovered Application Services \[cmdb\_ci\_service\_discovered\]. This Agent uses AI semantic search to find the best-matching discovered services for each business application and writes the relationship to \[cmdb\_rel\_ci\]. High-confidence matches are connected automatically. Medium-confidence matches are saved to a staging table for administrator review.


## Why these AI Agents are needed

Without these AI Agents, Service Mapping administrators have to manually review each ML-powered candidate and decide whether to create a service map. Similarly, connecting discovered application services to their business application context in the CSDM required manual one-to-one or one-to-many mapping. Using the AI Agents makes these processes significantly less time-consuming and enables processing at a much larger scale.

The following examples illustrate the challenges these AI Agents solve.

Consider a bank that has a payment application defined as a business application. Under it, Service Mapping discovers many application services: online payment processing, cash payment handling, net banking, and mobile payment systems. Business stakeholders are only concerned with the payment application at the top level and need it connected to all the relevant discovered services so they can monitor health and impact. Manually maintaining these connections as new application services are created is impractical. The Business App Mapping AI Agent solves this by iterating over all business applications and automatically finding and connecting the matching discovered services, working top-down from the smaller set of business applications to the larger set of discovered application services.

In a typical scenario, an organization runs hundreds of servers and generates a large number of ML-powered candidates daily. A Service Mapping administrator who previously had to manually evaluate each candidate and create a service map can instead activate the Service Mapping AI Agent, which processes all high-confidence candidates automatically, creates service maps, and sets them to non-operational for administrator review.

## How AI Agents work

Both agents use a ReAct \(Reasoning and Acting\) strategy. The agent reasons about each step before deciding which tool to invoke. After activation, a script runs every 15 minutes. On each run, the agent processes all relevant records in a single batch — for example, all business applications in the system — without any per-record input from an administrator.

Service Mapping AI Agent process:

1.  The agent retrieves full ML candidate data from the Application Service Candidate \(ASC\) record, including the candidate name, process name, and server count.
2.  The agent performs a noise check. If the candidate is flagged as noise, such as monitoring clients, security clients, or operating system processes, the agent skips it.
3.  The agent retrieves all running processes associated with the candidate.
4.  The agent analyzes the data and reasons about what the actual service is, prioritizing candidates with a high-confidence name suggestion source such as Service Fingerprints \(SFPs\).
5.  The agent creates the service topology in the CMDB and sets the service to non-operational. If a topology for the same candidate already exists, the agent skips creation.

Business App Mapping AI Agent process:

1.  The agent retrieves all Business Application records from \[cmdb\_ci\_business\_app\].
2.  For each business application, the agent runs an AI semantic search against \[cmdb\_ci\_service\_discovered\] using the application name and description as the query. The search returns up to 30 candidates, ordered by relevance score \(0–1\).
3.  Candidates with a score of 0.3 or higher are automatically connected. The agent creates a Uses::Used by relationship in \[cmdb\_rel\_ci\]. A business application can be linked to multiple services if multiple candidates qualify.
4.  Candidates with a score of 0.1–0.29 are saved to the staging table \[sn\_sm\_gen\_ai\_ba\_candidate\_rel\] for administrator review. No relationship is created automatically for these.
5.  Candidates below 0.1 are filtered out. The agent does not create a record or a relationship for these.

**Note:** If the AI Search profile is unavailable, the Business App Mapping AI Agent falls back to a keyword search using the `CONTAINS` operator on the service name field.

## Activation and monitoring

Both agents are inactive by default. A user who has the Service Mapping admin role activates them from the Service Mapping home page. For procedural information, see [Activate AI Agents for Service Mapping](../task/activate-sm-ai-specialists.md).

No configuration in AI Agent Studio is required for Service Mapping administrators; AI Agent Studio is used by platform administrators or users who have the AI admin role to manage agent definitions and token usage.

After activation, both agents run automatically every 15 minutes. Administrators can monitor activity and review results in the **AI Activity** section of the Service Mapping list navigation. For more information, see [Service Mapping AI Agent activity list tables](../reference/sm-ai-specialist-activity-columns.md).

Service maps created by the Service Mapping AI Agent are non-operational by default and can be made operational from the application service record in the Mapped Application Services list.

## AI Agent processing quota

Each AI Agent can process up to 100 records by default. When an AI Agent reaches this limit, it stops processing and its status is set to **Paused**. The AI Agent can be reactivated only after increasing the quota through the AI Agent Studio. To increase the quota, contact your AI administrator.

-   **[Activate AI Agents for Service Mapping](../task/activate-sm-ai-specialists.md)**  
Activate the Service Mapping AI Agent and the Business App Mapping AI Agent from the Service Mapping home page to start automated service map creation.
-   **[Service Mapping AI Agent activity list tables](../reference/sm-ai-specialist-activity-columns.md)**  
Use this reference to interpret the tables in the Service Mapping AI Agent activity list.
-   **[Business App Mapping AI Agent confidence thresholds](../reference/sm-ai-specialist-confidence-thresholds.md)**  
Use this reference to understand how the Business App Mapping AI Agent handles matches based on their AI confidence score, and what action is taken for each score range.

**Parent Topic:**[AI capabilities in Service Mapping](ai-workflows-service-mapping.md)

