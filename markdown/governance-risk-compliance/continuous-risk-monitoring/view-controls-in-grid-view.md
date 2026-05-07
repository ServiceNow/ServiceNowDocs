---
title: View controls in grid view
description: View and edit controls and their requirements in a hierarchical data grid that enables bulk operations and in-line editing.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 1
breadcrumb: [RMF step 3 - Implement controls, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# View controls in grid view

View and edit controls and their requirements in a hierarchical data grid that enables bulk operations and in-line editing.

## Before you begin

Role required: sn\_grc\_cam.manager, sn\_grc\_cam.admin, or sn\_grc\_cam.isso

## About this task

The Controls tab displays a hierarchical data grid where you can expand controls to view their requirements. The grid view enables you to edit multiple controls without navigating between records. This enables you to add implementation statements or perform bulk operations.

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace** and select the **List** icon.

2.  From the **Authorization packages** in the RMF list, select an authorization package.

3.  Select the **Controls** tab.

    The hierarchical grid view displays by default, showing controls with expandable requirements.

4.  To expand a control and view its requirements, select the expand icon next to the control.

5.  To expand all controls at once, select the expand icon in the Reference column heading.

6.  To open a control or requirement record, select the link in the Reference column.


## What to do next

**Edit implementation statements:**

-   Select the **Implementation Statement** cell
-   Enter or modify the text
-   Implementation statements are editable only when control state is in Draft and the authorization package is in Implement step

**Edit attestation respondents:**

-   Double-click the **Attestation Respondents** cell
-   Add or remove respondents
-   Attestation respondents are editable throughout the lifecycle regardless of state

**Create attestations:**

-   Select one or more controls
-   Select **Attest**
-   The system creates attestation records and updates control state to Attest

**Customize columns:**

-   Select the three-dot menu icon
-   Select **Personalize Columns**
-   Show or hide columns as needed

