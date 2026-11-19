---
title: Privacy content accelerator
description: The Privacy content accelerator provides prebuilt privacy compliance content that privacy users can activate directly from the Privacy workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/privacy-workspace/privacy-content-accelerator.html
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-10"
reading_time_minutes: 2
breadcrumb: [Privacy Management, Governance, Risk, and Compliance]
---

# Privacy content accelerator

The Privacy content accelerator provides prebuilt privacy compliance content that privacy users can activate directly from the Privacy workspace.

## Disclaimer

**Important:**

The ServiceNow Risk products help customers address regulatory requirements under various jurisdictions. However, we do not guarantee compliance and customers are ultimately responsible for their own compliance with applicable regulations.

ServiceNow aims to provide software updates for new or updated major regulations and requirements within twelve to eighteen months of the regulation's publication. For regulations for which ServiceNow provides a level of support in the base system, ServiceNow aims to provide software updates for minor regulatory changes within 12 months and for major regulatory changes within up to 18 months depending on scope and impact. We differentiate between typical regulatory content updates, which do not require software updates or enhancements, and regulatory updates, which do require software updates or enhancements. Content updates are generally delivered on a shorter cadence than if software update or enhancement is required for the regulatory update or change.

## Accessing the privacy content accelerator

The Privacy content accelerator provides pre‑built authority documents, citations, control objectives, and risk statements aligned with major privacy frameworks, including GDPR, CCPA, LGPD, and the NIST Privacy Framework 1.0.

A dedicated icon in the Privacy workspace provides navigation to the privacy content accelerator. Only users with the Privacy Manager or Privacy admin roles can view and access this icon.

## Content tab

The privacy content accelerator page contains two tabs:

-   Privacy Frameworks: Displays four authority documents. Each authority document card shows the count of related citations and control objectives. The card also shows the current status and the version number \(when an active version exists\).
-   Risk Statements: Displays risk statement categories. Each category card shows the version and provides an option to activate the associated risk statements.

## Authority document status

Each authority document card reflects one of the following statuses:

-   New: The authority document has not been installed. The card displays an **Activate** button.
-   Active: The authority document is installed. The card displays the active version number and an **Update** button.

## Installation states for citations and control objectives

Individual citation and control objective records display an installation state:

-   **Ready** — The record has not yet been installed.
-   **Installed** — The record is installed and active in the instance.

When an authority document is activated or updated, selected citations and control objectives transition from **Ready** to **Installed**.

## Overwrite behavior for existing records

If a citation with the same name already exists in the instance and it belongs to the same authority document, installing the content pack version overwrites the existing record.

## Parent citations

Citations may reference parent citations. If a parent citation has not been installed, the parent field on child citation records displays an empty value. The parent citation value is populated after the parent citation is installed. The same behavior applies to related control objectives.

## Content reference records

When an authority document is activated, a content reference record is created. This record stores the active version and links to all citations installed for that authority document. Each citation record, in turn, lists its associated control objectives.

## Risk statements

The Risk Statements tab in the privacy content accelerator displays risk statement categories. Each category is represented as a card that shows the version of the available content.

