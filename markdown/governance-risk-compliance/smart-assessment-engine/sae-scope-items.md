---
title: Scope items in an assessment
description: The scope of an assessment is the specific record that the assessment targets — such as a control, vendor, or entity. Scope items keep that record in view for responders and reviewers, and other SAE features use scope to behave intelligently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/sae-scope-items.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 4
keywords: [scope, scope item, assessment scope, scope items, reference information]
breadcrumb: [Triggering assessments, Configure, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Scope items in an assessment

The scope of an assessment is the specific record that the assessment targets — such as a control, vendor, or entity. Scope items keep that record in view for responders and reviewers, and other SAE features use scope to behave intelligently.

## Scope item overview

An assessment is never a questionnaire in the abstract — it is always completed *about* something specific. That "something specific" is the assessment's scope. A scope item is a pointer to a single source record. It is identified by a table \(for example, the *Vendor* table\) and a record on that table \(for example, *Acme Corp*\). An assessment can have one scope item, multiple scope items, or none.

Two assessments built from the same template can have completely different answers because they are scoped to different records. For example, a vendor security questionnaire scoped to *Acme Corp* and the same questionnaire scoped to *Globex Inc* share the questions but capture each vendor's own answers.

A useful way to think about it:

-   **The template**

    Defines *what* to ask \(questions, sections, instructions\).

-   **The scope**

    Defines *about what* to ask it \(the source record\).

-   **The responder**

    Provides the answers.


Scope items aren't configured on a template or template category. Scope is assigned at the time the assessment is created — typically through an assessment trigger, a Flow Designer action, or a public API call. Once an assessment is created, responders, reviewers, and administrators can view its scope items but can't add, change, or remove them from the responder experience.

## Where scope items appear in the assessment

Scope items appear in several places so that responders and reviewers can keep the source record in view as they work.

-   **Assessment header**

    The header at the top of the assessment shows scope items inline alongside the assessment title and status. Each scope item is shown as a label \(the source table name\) and a value \(the source record name\).

-   **Navigation panel \(combined assessments\)**

    The left navigation panel renders scope items on each assessment card so responders can distinguish constituent assessments. When assessments share the same template, scope items appear in a stacked layout. When templates differ, scope items appear in a tabbed layout.

-   **Section viewer**

    The section viewer header displays scope items for the constituent assessment in a tabbed layout. This keeps the source record in view while responders answer questions.

-   **Details / contextual sidebar**

    The Details section includes a Scope card that lists every scope item as a label-value pair. When reference fields are configured for a scope item, an additional reference information card appears. It surfaces the configured fields from the source record in a breadcrumb-style layout \(for example, **Department** &gt; **Cost center** &gt; **Manager**\).

-   **Assessment task list**

    The list of assessments that a reviewer or assignee sees before opening any one of them surfaces scope item fields as columns on each row. This makes it easier to triage and prioritize work across many assessments without having to open each one.


In the assessment header, navigation panel, and section viewer, no more than three scope items are shown at a time. If an assessment has more than three scope items, the additional items are summarized as a **+ N more** indicator. Selecting the indicator opens a tabbed popover that lists every scope item on the assessment.

## Setting scope items on an assessment

Scope items are set when the assessment instance is created. The supported entry point is Assessment trigger or Flow Designer action. This pass scope items as an input parameter when triggering the assessment.

Each scope item is an object with a **table** value \(the source table name\) and a **record** value \(the sys ID of the source record\). Scope items are cascade-deleted when the assessment instance is deleted.

## Roles and access

Scope items follow the access model of the assessment instance:

-   **sn\_smart\_asmt.assessment\_admin**

    Can view and modify scope items at the table level. Typically used by administrators who configure assessment triggers and Flow Designer actions.

-   **sn\_smart\_asmt.actor**

    Can view scope items on assessments assigned to them. Scope items are read-only from the responder experience.

-   **sn\_smart\_asmt.assessment\_reader**

    Can view scope items on assessments that they have read access to. Scope items are read-only.

-   **sn\_smart\_asmt.reassign**

    Can view scope items as part of the in-progress assessments that they reassign to another user.


## Tables used by the scope feature

The assessment scope is supported by two tables in the Smart Assessment Engine data model:

-   **Scope item \[sn\_smart\_asmt\_scope\_item\]**

    Identifies a single source record by table name and record sys ID.

-   **Assessment instance to scope item \[sn\_smart\_asmt\_m2m\_instance\_scope\_item\]**

    Links an assessment instance to one or more scope items.


For a full list of tables installed by Smart Assessment Engine, see [Tables installed in Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/tables-installed-in-smart-assessment-engine.md).

