---
title: Understanding processing activity hierarchy
description: Track how personal data flows across vendors, applications, and systems within and beyond a processing activity to identify and mitigate privacy-related risks.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
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

**Parent Topic:**[Processing activities](ropa-record.md)

