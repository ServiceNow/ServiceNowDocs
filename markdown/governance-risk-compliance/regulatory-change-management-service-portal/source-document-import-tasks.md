---
title: Source document import tasks
description: The Regulatory Change Management application processes external alerts that may include citation titles, citation numbers, and references to legislative or regulatory materials relevant to compliance.
locale: en-US
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Regulatory process flow and tasks, Explore, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Source document import tasks

The Regulatory Change Management application processes external alerts that may include citation titles, citation numbers, and references to legislative or regulatory materials relevant to compliance.

Each alert record contains metadata that supports the import of the document into the regulatory library. The metadata includes citation names and other relevant reference information for proper classification and traceability.

Regulatory alerts of the source document type provide citation titles and citation numbers when received. Source documents may reference legislative or regulatory materials relevant to compliance and governance.

Unassigned source document alert records are assessed to determine applicability. If marked as applicable, a source document import task is created automatically. The import task originates from the regulatory alert record and follows a defined workflow or life-cycle. The source document import life-cycle begins when the alert is marked applicable by a user with the `sn_grc_reg_change.manager` role. The import document task then appears in the Ready to import state for stakeholder review.

Compliance team members evaluate the citation associated with the alert and determine the appropriate action. Each import task facilitates ingestion of a specific source document into the regulatory library. Compliance team members are responsible for importing the document and maintaining consistency within the regulatory library.

You can associate multiple source document import tasks with a single regulatory alert. This configuration simplifies management and improves tracking of regulatory content ingestion processes. Each task adds relevant documents to the regulatory library for comprehensive capture and organization. Grouping tasks under one alert enhances traceability throughout the regulatory change management process.

## New workflow of a source document import task

Upgrade the following applications to get the new workflow:

-   GRC: Common Workspace Elements \(`sn_grc_workspace`\)
-   GRC: Regulatory Change Management \(`sn_grc_reg_change`\)

Starting with version 19.0.x, a source document task progresses through the following states:

-   Ready to Import- The task has been identified and prepared for import into the system. No work has started yet.
-   In Progress- The task is actively being worked on. This includes analyzing the source document and defining necessary regulatory changes.
-   Implementation- Identified changes are being executed. This may involve creating related tasks such as policy updates, control modifications, or process changes.
-   Awaiting Approval- All implementation activities are complete, and the task is pending review and approval from the appropriate stakeholders or compliance team.
-   Closed- The task has been reviewed, approved, and all required actions are completed. No further work is needed.

**Parent Topic:**[Regulatory process flow and tasks](reg-change-workflow-swimlane.md)

