---
title: Understanding processing activity hierarchy
description: Track how personal data flows across vendors, applications, and systems within and beyond a processing activity to identify and mitigate privacy-related risks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/privacy-workspace/processing-activity-hierarchy.html
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Processing activities, Explore, Privacy Management, Governance, Risk, and Compliance]
---

# Understanding processing activity hierarchy

Track how personal data flows across vendors, applications, and systems within and beyond a processing activity to identify and mitigate privacy-related risks.

Each processing activity can involve multiple entities such as vendors, applications, and systems that together make up the processing activity. These vendors, applications, and systems share data with each other, making it essential to establish a lineage that tracks where personal data is shared. This understanding helps organizations identify and mitigate privacy-related risks.

## Scenario to understand the importance of Hierarchy

To understand why lineage is important, consider the following example of a Talent Screening processing activity:

-   A candidate registers on the careers portal and submits their resume.
-   The candidate's data is fed into SHL, an application used to conduct online assessments, to shortlist candidates.
-   Candidates who clear the SHL assessment have their data shared with HireVue for interviews.
-   Simultaneously, cleared candidates' data is shared with Tableau for analytics purposes.

By establishing a lineage for this processing activity, the organization can track where each piece of personal data originates, how it is processed, and where it is shared. This visibility helps identify potential privacy risks, such as unauthorized access or data breaches, at any point where personal data is exchanged. With a clear lineage in place, the organization can ensure it is aware of all points where personal data flows and can implement appropriate safeguards to mitigate privacy-related risks.

## Lineage maps and data transfers

Each relationship that you define in a hierarchy is rendered as a lineage map. For more information, see [View lineage map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/hierarchy-tab.md).

When personal data moves between nodes in a hierarchy, privacy teams must track where the data goes, whose data is involved, and which legal safeguards permit each movement. Data transfer records capture this information on the processing activity. Each record represents a specific movement of personal data from one node to another, across regions. For more information, see [Manage data transfers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/data-transfers.md).

## Hierarchies, lineage maps, data transfers, and transfer mechanisms

|Function|Description|
|--------|-----------|
|Hierarchy|Defines how a processing activity connects to vendors, applications, processes, companies, and other entities. To create a relationship, see [Add relationships to a hierarchy for a processing activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/create-a-data-lineage-for-a-processing-activity.md).|
|Lineage map|Renders the hierarchy as a visual map so you can trace how data moves between all connected entities. For more information, see [Manage data lineage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/lineage.md).|
|Data transfer|Captures each distinct movement of personal data from one node to another.|
|Transfer mechanism|Associates every data transfer with a legal safeguard that governs it.|

**Parent Topic:**[Processing activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/ropa-record.md)

