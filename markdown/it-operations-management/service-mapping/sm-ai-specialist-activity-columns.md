---
title: Service Mapping AI Agent activity list tables
description: Use this reference to interpret the tables in the Service Mapping AI Agent activity list.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-04-16"
reading_time_minutes: 1
keywords: [AI Agent activity, mapping results, ITOM]
breadcrumb: [AI Agents for Service Mapping, AI capabilities in Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping AI Agent activity list tables

Use this reference to interpret the tables in the Service Mapping AI Agent activity list.

<table><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the service map created or evaluated by the AI Agent.

</td></tr><tr><td>

Mapping results

</td><td>

The outcome of the mapping attempt:

 -   **Map created** – The AI Agent successfully created a new service map.
-   **Already exists** – A service topology already exists for this candidate; the agent skipped creation.
-   **Missing service context** – The agent could not identify a valid service from the candidate data.
-   **Missing data** – Insufficient candidate data was available to create a map.
-   **Failed** – The mapping attempt failed.

</td></tr><tr><td>

Created

</td><td>

The date and time the activity record was created.

</td></tr></tbody>
</table><table><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the business application.

</td></tr><tr><td>

Application service mapped

</td><td>

The application service that the Agent identified as a match.

</td></tr><tr><td>

Mapping results

</td><td>

The outcome of the mapping attempt:

 -   **Linked** – The AI Agent found a matching application service for the business application and automatically created a "Uses::Used by" relationship between them.
-   **Already connected** – The relationship between the business application and the application service was created manually.
-   **Needs review** - The AI Agent identified a possible match between the business application and an application service, but the confidence level was not high enough to create the relationship automatically.
-   **No match found** - The AI Agent did not find an application service that could be linked to the business application with sufficient confidence. No relationship was created.
-   **Failed** – The AI Agent has failed to link between the business application and the service instance.

</td></tr><tr><td>

Confidence

</td><td>

The AI confidence level for the mapping: High, Medium, or Low.

</td></tr><tr><td>

Created

</td><td>

The date and time the activity record was created.

</td></tr></tbody>
</table>**Parent Topic:**[AI Agents for Service Mapping](../concept/service-mapping-ai-specialists.md)

