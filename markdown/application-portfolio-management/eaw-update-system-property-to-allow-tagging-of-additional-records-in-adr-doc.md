---
title: Enable referencing additional records in architectural decision records
description: You can customize the default values of the sn\_apm\_ws.record\_mention\_config system property, to enable the tagging of additional record tables in an architectural decision record \(ADR\).
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage architectural decision records \(ADR\), Working with information portfolio, Working with Portfolio list view, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Enable referencing additional records in architectural decision records

You can customize the default values of the **sn\_apm\_ws.record\_mention\_config** system property, to enable the tagging of additional record tables in an architectural decision record \(ADR\).

## Before you begin

Role required: sn\_apm.apm\_admin

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  From the system properties list, locate and open the **sn\_apm\_ws.record\_mention\_config** system property.

3.  In the **Value** field, add the details of the record table that you want to tag in the ADR docs component.

    For example, if you want to tag records from the Business application table \(**cmdb\_ci\_business\_app**\) in the ADR docs component, add the table details to the array in the following format.

    ```
      {
        "sourceTable": "cmdb_ci_business_app",
        "filterCondition": "",
        "label": "Business application",
        "fields": [
          "name"
        ]
      }
    
    ```

    In the format, you must enter the relevant information in the following rows:

    -   **sourceTable**: Enter the source table from where you want to tag data in the ADR docs component.
    -   **label**: Enter the name of the source table that will be displayed in the **Mention a record** context menu when you enter **/** in the ADR docs component.
4.  Select **Update**.

    You can start tagging records from the new table in the ADR docs component. For more information, see [Tag users or records in Architectural Decision Records](eaw-tag-users-or-records-in-adr.md).


**Parent Topic:**[Manage architectural decision records \(ADR\)](../../concept/eaw-concept/eaw-manage-adr.md)

**Related topics**  


[Tag users or records in Architectural Decision Records](eaw-tag-users-or-records-in-adr.md)

[Add or edit an architectural decision record \(ADR\)](eaw-create-edit-adr.md)

[Request approval for an architectural artifact version of type Architectural Decision Record](eaw-request-approval-adr.md)

[Create and manage pages and subpages for architectural decision records](eaw-create-and-mng-page-subpage-for-adr.md)

[Add an architectural decision record version](eaw-add-an-adr-version.md)

