---
title: Step 4. Create a view for a new Linked Record Tab for a Security Case
description: Customize the List layout for a Security Case table when it is displayed on the Link Records page with the Major Security Incident Management workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/creating-a-view-for-the-new-linked-record-tab.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Rollup example use case implementation for a Security Case, Rollup Framework for MSIM, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Step 4. Create a view for a new Linked Record Tab for a Security Case

Customize the List layout for a Security Case table when it is displayed on the Link Records page with the Major Security Incident Management workspace.

## Before you begin

**Prerequisites:**

-   Choose the column that should be visible when a list is rendered for a Security Case table.
-   Choose the order of the fields to be displayed in the drop-down list.

Role required: admin

## Procedure

1.  Search for **sn\_msi\_m2m\_child.list** using the left navigation.

    The Linked Records table is displayed.

2.  Select and hold \(or right-click\) the header and select **Configure** &gt; **List Layout**.

    The Configuring Linked Records List page is displayed.

3.  Go to **List View** &gt; **View name**.

4.  Select **New** from the View name drop-down list.

    \[Omitted image "view-name-new-step4.png"\] Alt text: List view name.

5.  Select the columns that will render on the workspace list view.

    The security case record is stored in the **Number** column. To render information from a security case, you must dot walk on the **Number** column.

    \[Omitted image "view-name-security-case-step4.png"\] Alt text: Security Case view name.

    1.  To dot walk, first select the **Number** column from the Available list and then select **Expand Selected Reference Field**.

        \[Omitted image "view-name-security-case-expand-step4.png"\] Alt text: Expand view.

    2.  Expand the columns from **Number** to select and move them to the Selected list.

        \[Omitted image "view-name-expanded-view-step4.png"\] Alt text: Expanded view name.

    3.  Click **Save** to save and create a view.
6.  The next step is to render the created view within the Major Security Incident Management workspace, you need to create a **List Layout Configuration**.

    1.  Search for the **List Layout Configuration** using the left navigation.
    2.  Select **MSI Administration** &gt; **List Layout configurations**.
    3.  Select **New** to create a new configuration.
    4.  Select the source table from the Table column and select the newly created view from the List View field.
    5.  The **List View** label enables you to control labels when the same source table is rendered in the Major Security Incident Management workspace.
    6.  **Save** the record.

        **Note:** After the record is saved, navigate to Major Security Incident Management workspace to view the rendered list view and label within the workspace.

        \[Omitted image "list-layout-step4.png"\] Alt text: List layout.


**Parent Topic:**[Rollup example use case implementation for a Security Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/use-case-for-a-security-case.md)

