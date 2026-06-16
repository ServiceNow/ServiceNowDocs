---
title: Guided Decisions Experience release notes
description: Version history for the Guided Decisions Experience application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-guided-decisions-experience.html
release: store
topic_type: reference
last_updated: "2026-02-05"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Guided Decisions Experience release notes

Version history for the Guided Decisions Experience application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 41.0.1 - February 2026**

    New: Introduced a new playbook activity, Guided Decision with Inputs and Outputs, which allows you to pass inputs into decision trees and reuse their outputs across subsequent playbook activities.

-   **Version 39.0.2 - December 2025**

    Fixed: Minor fixes for this release.

-   **Version 38.0.1 - September 2025**

    Fixed: A bug has been fixed to display the questions or guidances correctly when editing a previous node in a decision tree.

-   **Version 37.0.1 - August 2025**

    Minor bug fixes for this release.

-   **Version 35.0.1 - May 2025**

    Fixed: Minor bug fixes for this release.

-   **Version 34.0.1 - February 2025**

    Includes bug fixes.

-   **Version 33.0.5 - January 2025**

    Bug fix.

-   **Version 33.0.4 - December 2024**

    Fix for 500 internal server error caused by slower responses when executing large decision trees with many nodes and multiple input mappings.

-   **Version 33.0.3 - November 2024**

    Includes bug fixes.

-   **Version 33.0.2 - September 2024**
    -   Ability to use previous responses of a decision tree in a question.
    -   Ability to include knowledge article to answer the questions in a decision tree by enabling a system property \(sn\_gd\_core.include\_knowledge\_articles\_in\_decision\_tree\).
-   **Version 30.0.1 - August 2024**
    -   Added support to add rich text and images to questions in decision tree using html editor.
    -   Users can start a decision tree with only task input.
    -   Ability to retrigger a decision tree in a playbook which begins a new execution of the tree on every trigger.
    -   Decision trees are made searchable in portal through AI Search.
    -   Add decision tree as a catalog content type to help surface decision trees in service catalog.
-   **Version 29.0.2 - June 2024**

    Fixes including showing choices in user session language.

-   **Version 29.0.0 - May 2024**
    -   Fixed WCAG and localization defects.
    -   Output modal while creating decision trees.
    -   Added validation access to all decision tree run time APIs based on user criteria associated with corresponding record.
    -   Decision tree author will now be allowed to end a decision tree with a guidance node or decision node.
    -   Added confirmation popover for intermediate node.
    -   Enabled outputs in linking node.
    -   Decision tree author is enabled to map inputs/outputs to decision tree outputs.
    -   Decision tree author can now add a decision node after a linking node.
    -   Expose widgets to snc\_external users.
    -   Enabled to create portal search result page with decision tree widget.
-   **Version 27.0.0 - February 2024**
    -   Changes to Decision Tree Builder to support nested decision trees. This allows decision tree author to link an activated decision tree inside the current decision tree.
    -   Ability to expose guided decision experience in the portal using the decision tree widget for internal users.
    -   Changes to allow returning to or editing of any answer or guidance in a decision tree.
    -   Theming updates for Decision Tree Builder.
-   **Version 26.2.1 - November 2023**
    -   Fixes for decision tree builder validations and condition builder
    -   Styling fixes.
-   **Version 26.1.2 - August 2023**
    -   Changes for builder theming.
    -   Accessibility changes and fixes for Decision Tree Builder experience.
-   **Version 24.4.0 - November 2022**

    Major refactoring of code to improve performance.

-   **Version 23.0.1 - August 2022**

    Guided Decisions guides agents through a set of questions to determine the action that will help them resolve an issue or complete a task in the most optimal way. It asks them questions based on previous answers and gives guidance on the next step in the resolution process. Guided Decisions reduces the cognitive burden on agents and improves their productivity. Guided Decisions can be embedded in a Playbook or served as a Recommended Action.


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

