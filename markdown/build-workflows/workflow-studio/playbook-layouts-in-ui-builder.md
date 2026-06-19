---
title: Playbook layout bundles
description: Playbook layout bundles are pre-wired component sets in UI Builder that determine how a playbook renders for end users at runtime. Each bundle packages a controller, supporting components, and styling so that authors can drop a complete playbook experience onto a page without configuring each component individually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/playbook-layouts-in-ui-builder.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 2
breadcrumb: [Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Playbook layout bundles

Playbook layout bundles are pre-wired component sets in UI Builder that determine how a playbook renders for end users at runtime. Each bundle packages a controller, supporting components, and styling so that authors can drop a complete playbook experience onto a page without configuring each component individually.

Choose a bundle based on how you want end users to move through the playbook. Some bundles let users navigate freely between activities and stages. Others restrict navigation to a sequential flow, which is useful when the playbook depends on decisions that should be answered in a specific order.

You add bundles to a page from the Content panel, then select **Components** and filter by **Playbook**. Select the bundle you want and drop it onto the page. The bundle auto-wires its controller and components.

\[Omitted image "playbook-all-layouts.png"\] Alt text: Screenshot showing all playbook layouts in the UI Builder.

-   **Playbook**

    The core bundle for displaying a playbook. Other bundles build on this foundation.

-   **Playbook Form**

    Renders the form controls for a playbook activity. Used when an activity requires user input or data entry.

-   **Playbook Modals**

    Provides modal dialogs for playbook interactions, such as confirmations, errors, or supplementary forms.

-   **Playbook Activity Picker**

    Displays a list or menu of activities that end users can select to navigate to a specific activity within a stage. Typically appears as a left-side panel in layouts that use non-sequential navigation.

-   **Playbook Guided Layout**

    Renders the playbook as a guided experience, removing the activity picker and stage picker so end users progress sequentially through the decisions and activities. Previous responses are consolidated into an accordion below the active activity. Use for Guided Decision Playbooks. There is no matching page template. You add the bundle to a page you create from scratch or from the Standard record template.

-   **Playbook Stage Picker**

    Displays the stages of a playbook so end users can navigate between them. Typically appears as a top bar in multi-stage playbooks.

-   **Playbook Activity Viewer**

    Renders the content of the active playbook activity. Used in layouts where the activity content needs to be displayed independently of pickers or navigation controls.

-   **Playbook Focused Vertical**

    Displays one activity at a time in a vertical layout, with full focus on the current step. Use for multi-stage playbooks where end users should concentrate on one activity before moving to the next. Has a matching page template.

-   **Playbook Stacked Vertical**

    Displays multiple activities stacked vertically, allowing end users to see and interact with several activities on the same page. Use when context across activities is helpful. Has a matching page template.

-   **Playbook Horizontal Wizard**

    Renders the playbook as a wizard with discrete numbered steps along the top of the page. Use for linear playbooks where each step builds on the previous one. There is no matching page template. You add the bundle to a page you create from scratch or from the Standard record template.

-   **Playbook Focused Horizontal**

    Displays one activity at a time in a vertical layout, with full focus on the current step. Use for multi-stage playbooks where end users should concentrate on one activity before moving to the next. Has a matching page template.

-   **Playbook Stacked Horizontal**

    Displays multiple activities in a horizontal arrangement \(alternative to Stacked Vertical\). Use for layouts where horizontal flow fits the workspace or screen better than a vertical stack. Has a matching page template.


