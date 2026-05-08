---
title: Assignment Configurator for non-regulatory alerts
description: Assignment rules help in automating organization’s task records such as action tasks, and non-task records such as issues, incidents, regulatory alerts, and so on.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Assignment Configurator for non-regulatory alerts

Assignment rules help in automating organization’s task records such as action tasks, and non-task records such as issues, incidents, regulatory alerts, and so on.

The Assignment Configurator module allows you to automatically set a value in the assigned\_to and assignment\_group fields when a set of conditions occurs and applies to Integrated Risk Management record-based tables such as issues, incidents, compliance cases, risks, controls and many more.

An assignment rule must also meet these additional criteria to run:

-   The task record has been created or updated. Assignment rules do not apply to unsaved changes on a form.
-   The task record must be unassigned. The record cannot have an existing value for either the `assigned_to` or `assignment_group` fields. Assignment rules cannot overwrite existing assignments \(including assignments set by a default value or a previously run assignment rule\).
-   The assignment rule is the first rule that matches the table and conditions. If more than one assignment rule matches the conditions, only the rule with the lowest order value runs.

-   **[Configure assignments](configure-assignments.md)**  
Assignment configuration rules help in automating organization’s task records such as action tasks, and non-task records such as issues, incidents, regulatory alerts, etc.

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

