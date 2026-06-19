---
title: Collaboration in assessments
description: Collaboration in Smart Assessment Engine enables you to add multiple contributors to an assessment and support live collaboration with real-time updates. It also displays presence indicators to show who is active on the assessment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/collaboration-in-assessments.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Respond to assessments, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Collaboration in assessments

Collaboration in Smart Assessment Engine enables you to add multiple contributors to an assessment and support live collaboration with real-time updates. It also displays presence indicators to show who is active on the assessment.

## Exploring Collaboration

The Collaboration feature in the Smart Assessment Engine aims to enhance the efficiency and effectiveness of team-based assessments by enabling multiple users to work together in real-time. It enables assessments to be assigned and reassigned to contributors, with simultaneous editing supported, each user's changes appear instantly to others. Presence indicators also show who are currently active on the assessment.

To support larger and more complex assessments, collaboration is extended through Granular Delegation, introducing section-level responsibility and access control. Granular delegation enables owners to assign contributors to entire assessments or specific sections, confirming subject matter experts focus only on relevant areas, improving efficiency, and assessment quality overall. Access follows a hierarchical model, when a user is granted access to a section, they automatically inherit access to all subsections within that section. As a result, teams can work together smoothly while maintaining clear ownership, strong data integrity, and visibility into individual responsibilities.

The Owner has the authority to assign or reassign the assessment and to add or remove contributors. Only the Owner can submit the assessment. Contributors can view the assessments assigned to them and see all participants listed in the side panel, but they cannot reassign or submit the assessment. Contributors can respond to questions and add comments and attachments to the assessment.

## Question-level communication

Each question card includes a dynamic panel with three question-level communication features:

-   **Comments**

    Comments anchored to a specific question. Reviewers and contributors can ask questions or raise concerns without referencing the assessment-level comment pane. Select the comment icon on a question card to open the conversation in the dynamic panel. Anyone with read access to the assessment can post a comment. When the assessment is in the Cancelled state, existing comments are read-only for all users. Script type questions don't support comments.

-   **Work notes**

    A private, role-restricted conversation thread beside the Comments tab. Work notes are intended for internal conversations between collaborators that should not be visible to all participants. A common example is comments exchanged between reviewers during a Third-Party Risk Management assessment that the vendor responder shouldn't see. Work notes are inactive by default. To make them available, an assessment administrator configures the **Work note roles** field on the template category with the roles that can view and post work notes. Users without a configured role don't see the Work notes tab.

-   **Question flags**

    A way to mark a question that needs attention. Flags have three states: Unflagged, Flagged, and Resolved. In a typical reviewer-responder loop, a reviewer flags a question to indicate an unsatisfactory response, the responder updates the answer, and the reviewer resolves the flag. Flagging is enabled for all roles by default. To restrict it, an assessment administrator configures the **Question flag roles** field on the template category with the roles that can change a question's flag state. Users without a configured role can still see the flag state but can't change it.


For details on configuring the **Worknote roles** and **Question flag roles** fields on a template category, see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md). For step-by-step responder workflows, see [Add a comment or work note to a question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/add-comment-to-question.md) and [Flag or resolve a question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/flag-a-question.md).

## Access levels and roles

Collaboration supports three distinct access levels, enabling primary owners to tailor permissions based on each contributor's responsibilities:

-   **Primary owner**

    The primary owner has full control over the assessment. They have the authority to:

    -   Assign or reassign the assessment to individuals.
    -   Add or remove assessment contributors and sectional contributors.
    -   Submit the assessment for review or completion.
    -   Respond to all questions across all sections.
    -   Manage comments and attachments made by all contributors.
-   **Assessment contributors**

    The assessment contributors have full read and write access to the entire assessment. They can:

    -   View the entire assessment, including all sections and questions.
    -   Respond to questions in any section.
    -   Add comments and attachments at the assessment level.
    -   See all contributors involved in the assessment.
-   **Sectional Contributors**

    Sectional Contributors provide targeted, granular access for users who should only work on specific sections of an assessment. They have:

    -   View the entire assessment, including all sections and questions.
    -   See all contributors involved in the assessment.
    -   Respond only to their assigned sections.
    -   Add comments and attachments at the assessment level.
    **Note:** Section Contributors see visual indicators \(lock icons\) on sections where they have read-only access, with clear messaging explaining their access level. This granular delegation enables primary owners to distribute assessment work across subject matter experts while maintaining centralized oversight.


## Benefits of Collaboration

Collaboration in Smart Assessment Engine enables multiple stakeholders to contribute, review, and refine content in real-time. It introduces flexibility, accountability, and improved quality into the process.

-   Tasks can be distributed and completed in parallel, significantly reducing turnaround time.
-   Every change is tracked, confirming accountability and offering a transparent view of who contributed what and when.
-   Collective expert knowledge results in more thorough and reliable assessments.
-   Large and complex assessments become manageable by dividing work among contributors.
-   Granular delegation supports diverse team structures, from full collaboration to highly targeted, section-specific assignments.
-   Section-level assignments create unambiguous responsibility for specific content areas, reducing confusion and overlap.
-   Primary owners retain full visibility and control while delegating specific work to others.
-   Question flags give reviewers and responders a structured way to raise and resolve concerns on individual questions before the assessment is finalized.
-   Question-level comments and work notes keep feedback anchored to the relevant question. Comments support general discussion; work notes provide private, role-restricted threads not visible to external participants.

Collaboration transforms assessments from isolated, siloed activities into dynamic, team-driven processes. By enabling structured collaboration, organizations can not only increase the quality and speed of assessments but also foster greater alignment, transparency, and decision-making confidence across teams.

