---
title: Embedded assessments
description: Upstream applications can embed the Smart Assessment Engine responder experience directly within their workspace and control which interface components are visible.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/embedded-assessments.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 7
keywords: [embedded assessments, compact mode, assessment responder, Smart Assessment Engine]
breadcrumb: [Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Embedded assessments

Upstream applications can embed the Smart Assessment Engine responder experience directly within their workspace and control which interface components are visible.

Embedded assessments enable upstream applications to integrate the Smart Assessment Engine responder experience within their own workspace. The embedding application controls which interface components are displayed, which affects the availability of certain features. Compact mode does not affect the standard assessment display.

**Note:** Depending on the embedded configuration, some assessment capabilities — such as collaboration features that depend on the reference info pane — may behave differently or be unavailable in the embedded view.

## Use cases for embedded assessments

Upstream applications typically embed an assessment in one of the following scenarios:

-   A record page that already represents the entity being assessed. For example, embedding a control attestation inside the Control record, or embedding a vendor security assessment inside the vendor record. Responders complete the assessment without leaving the parent record.
-   A playbook step that includes an assessment as part of a guided process. Embedding the assessment inline keeps the responder in the playbook flow and avoids opening a separate browser tab for the assessment.
-   A workspace landing page or related-list view that surfaces the assessment alongside other context, such as related incidents or audit history.

In each scenario, the upstream application configures the Smart Assessment component in UI Builder to fit the available space and remove duplicate UI elements, such as a second header or a second reference pane. For the configuration on the SAE side that supports embedding, see [Embed an assessment in a record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/embed-assessment-in-record-page.md).

## Header visibility and mode

In addition to showing or hiding the assessment header, the embedding application can set the header mode to one of the following:

-   **Standard mode**

    The full assessment header is shown, including the assessment name, scope item, requested and due dates, and the standard assessment actions. Use this mode when the embedded assessment occupies the entire page or when the parent context is not visible elsewhere.

-   **Compact mode**

    A reduced header is shown without the scope item. This mode is intended for cases where the embedded assessment sits inside a parent record page or playbook step that already shows the assessment context, so repeating the scope item would be redundant. The compact header still indicates auto-save status and exposes the assessment-level actions, but uses less vertical space.


The embedding application can show or hide the assessment header. When the header is hidden, consider the following:

-   Auto-save status must be indicated through an alternate mechanism to prevent data loss from unsaved form changes.
-   Action elements — including **Submit**, **Reassign**, and **Cancel** — must remain accessible through an alternate location. A filter action is optional.
-   Guidance information, including the assessment name and target record details, is not displayed.

**Note:** The header mode and header visibility properties apply in single mode only. In combined mode these property settings have no effect.

## Action visibility

Independently of the header mode, the embedding application can hide assessment-level actions individually or as a group:

-   **Hide all actions**

    A single property that hides every action on the assessment, including **Submit**, **Reassign**, and **Cancel**. Use this property when the embedding application provides its own action surface on the parent record and handles assessment lifecycle through its own controls.

-   **Hide Submit**

    Hides only the **Submit** action. The responder can't finalize the assessment from the embedded view; submission must be driven from the embedding application.

-   **Hide Reassign**

    Hides only the **Reassign** action. Reassignment must be performed from the standard assessment view or through a different control on the embedding application.

-   **Hide Cancel**

    Hides only the **Cancel** action. Cancellation must be performed by an administrator from the standard assessment view.


When any action is hidden, the embedding application is responsible for exposing an equivalent control elsewhere in the host UI so that responders and administrators can still complete the workflow.

The question filter dropdown is not part of the action set and remains visible in the header even when **Hide all actions** is selected. Responders can continue to filter the question list regardless of which actions are hidden.

**Note:** The action visibility properties apply in single mode only. In combined mode these property settings have no effect.

## Reference info pane visibility

The embedding application can show or hide the right reference info pane. Hiding this pane removes access to the following features:

-   Reference information
-   Comments
-   Attachments
-   Collaboration

**Note:** The reference info pane visibility property applies in single mode only. In combined mode this property setting has no effect.

## Navigation pane visibility and modes

The embedding application can show or hide the left navigation pane, or make it collapsible. Hiding this pane removes access to the following features:

-   Required question indicators
-   Section navigation

Progress indicators for the assessment aren't tied to the navigation pane. The progress remains available whether the navigation pane is pinned, opened through the trigger button, or hidden entirely. When the navigation pane is hidden, all sections are displayed sequentially in the center pane, each following the previous.

A single component property, **Pin navigation by default**, controls how the navigation pane is presented when the assessment loads. The property is selected by default; the responder can pin or unpin the pane at any time during their session:

-   **Pinned \(default\)**

    The navigation pane is expanded and fixed beside the question area. Section names are visible at all times.

-   **Not pinned**

    The pinned pane is hidden and a trigger button in the question area opens the navigation in a dialog. The responder can pin the pane from the dialog at any time. This option is intended for embedded contexts where horizontal space is limited.


In combined mode, the navigation pane remains pinned regardless of the **Pin navigation by default** property setting.

## Inheriting read access from a parent record

By default, access to an embedded assessment follows standard Smart Assessment role-based access rules. Any user with the relevant smart assessment role and access to parent record can view it. If you want to restrict visibility based on the parent record's audience, you can optionally enable parent record-based access inheritance on the template category. To configure this behavior, see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).

Configuring parent record-based access inheritance is optional. Without it, the embedded assessment functions normally with role-based access alone. Enabling it adds an additional access check — users must also have read access to the parent record.

When parent record-based access inheritance is enabled on the template category, a user must satisfy both of the following conditions at runtime to access an embedded assessment from this category:

1.  The user must have the Smart Assessment role required for the assessment.
2.  The user must have read access to the parent record for that template category.

## Configuration scope

Visibility properties — header mode, action visibility, reference pane visibility, navigation pane visibility, and pin-by-default — are set on the Smart Assessment component as it is added to a UI Builder page. They aren't set per assessment.

As a result:

-   Every assessment surfaced through the same UI Builder page uses the same visibility configuration.
-   Different UI Builder pages can embed the same assessment with different visibility settings. For example, one page can show the standard header while another page on a different record embeds the same assessment with a compact header and hidden actions.
-   To change visibility for a particular assessment in a particular host context, change the configuration of the Smart Assessment component on the UI Builder page that hosts it.

For the configuration steps on the SAE side, see [Embed an assessment in a record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/embed-assessment-in-record-page.md).

## Companion APIs for embedded scenarios

When the standard responder UI elements are hidden or constrained in an embedded view, the embedding application can drive the same operations through public APIs. These APIs are available regardless of how the Smart Assessment component is configured:

-   **Assessment state actions**

    The **Change Assessment State** Flow Designer action lets the embedding application transition an assessment to the Submitted or Cancelled state from its own UI when the corresponding header actions are hidden. The action performs the minimum required validations — state eligibility and required questions answered — before transitioning the state.

-   **Contributor management**

    A public API method on the Smart Assessment responder public API allows the embedding application to add or remove assessment-level contributors and section-level contributors programmatically. This is the recommended way to manage contributors when the reference info pane \(which hosts the standard contributor UI\) is hidden.


