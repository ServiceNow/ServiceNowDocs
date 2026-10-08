---
title: Ideal path for a playbook
description: The ideal path is the expected execution route through a playbook. The sequence of activities that should run when a decision resolves in the anticipated way. You can define an ideal path on each decision branch and visualize it across the entire playbook in Workflow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/ideal-path-for-playbook.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-08-21"
reading_time_minutes: 3
keywords: [ideal path, golden path]
breadcrumb: [Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Ideal path for a playbook

The ideal path is the expected execution route through a playbook. The sequence of activities that should run when a decision resolves in the anticipated way. You can define an ideal path on each decision branch and visualize it across the entire playbook in Workflow Studio.

When a playbook contains decision activities, each decision can branch in multiple directions depending on how conditions evaluate at runtime. In most processes, one branch represents the typical, expected outcome. For example, an approval decision that is usually approved. Marking that branch as the ideal path shows the route through the decision you intend as the norm.

The ideal path has two expressions in a playbook:

-   **In Workflow Studio**

    The Golden Path visualization traces a highlighted route through the canvas, following all configured ideal branches from start to end. Authors use this to confirm that their ideal branch selections add up to a coherent end-to-end path before activating the playbook.

-   **In the playbook runtime experience**

    Activities that are on the ideal path behind an unresolved decision are shown to the user as conditional activities. It displays a preview of what is likely to come next, even before the decision has been evaluated. When the decision resolves and execution follows the ideal path, the conditional activity becomes active. If execution takes a different branch, the conditional activity is replaced by the activity on the actual path taken.


## Ideal path and decision evaluation modes

The number of branches you can mark as ideal for a given decision depends on how that decision is configured to evaluate its branches.

-   **First matching branch only**: You can mark one branch as ideal.
-   **All matching branches**: You can mark multiple branches as ideal. All ideal branches are shown as conditional activities in the runtime experience simultaneously.

## How the Golden path visualization works

The Golden path visualization in Workflow Studio traces the ideal route through the entire playbook canvas when you enable **Golden path** from the **View options**. The following rules apply:

-   The playbook must contain at least one decision that has an ideal branch configured.
-   The visualization follows the ideal branch at each decision, highlighting all activities on that route in a golden color.
-   If a decision in the sequence has no ideal branch configured, the golden path highlighting stops at that decision. Activities after that point aren't highlighted, even if later decisions in the playbook do have ideal paths defined.
-   For decisions with multiple ideal branches configured, the golden path highlights all ideal branches from that decision forward.
-   The visualization updates when you undo or redo changes to ideal branch selections.
-   The visualization persists when you switch between playbook variants.

## How conditional activities work at runtime

Conditional activities are the runtime expression of the ideal path. They are shown as previews in the playbook execution view for activities that have not yet active because the decision that gates them has not yet resolved.

-   Conditional activities are read-only. Users can't interact with them until the decision resolves and execution reaches them.
-   When the decision resolves and execution takes a non-ideal path, the conditional activity is removed and the activity on the actual path is shown instead.
-   If the non-ideal path itself contains further decisions, those decisions can also have ideal branches configured, and their conditional activities are shown from that point forward.

Conditional activities are displayed only when the ideal path feature is enabled on the playbook experience record. By default, activities behind unresolved decisions aren't shown at runtime.

To learn about how to configure ideal path for a playbook in Workflow Studio, see [Configure the ideal path for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/configure-ideal-path-for-playbook.md).

-   **[Configure the ideal path for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/configure-ideal-path-for-playbook.md)**  
Mark one or more decision branches as the ideal path in Workflow Studio for a playbook. The playbook can highlight the expected execution route and show users a preview of upcoming activities at runtime.
-   **[Configure Playbook Experience to display ideal path](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/configure-playbook-experience-ideal-path.md)**  
Configure Playbook Experience to show the stages and activities in an ideal path before they are executed during a playbook run.

**Parent Topic:**[Creating and managing Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/creating-managing-playbooks.md)

