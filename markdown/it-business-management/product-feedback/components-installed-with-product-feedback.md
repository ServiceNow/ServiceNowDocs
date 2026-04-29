---
title: Components installed with Feedback application
description: Learn about several types of components installed with Feedback application in Strategic Planning such as user roles, tables, and, system properties.
locale: en-US
release: australia
product: Product Feedback
classification: product-feedback
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Feedback reference, Feedback application in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Components installed with Feedback application

Learn about several types of components installed with Feedback application in Strategic Planning such as user roles, tables, and, system properties.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Roles installed

<table id="table_evh_gkr_zzb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains role

</th></tr></thead><tbody><tr><td>

\[sn\_align\_core.pf\_read\]

</td><td>

Can view the Feedback.

</td><td>

None

</td></tr><tr><td>

\[sn\_apw\_advanced.pf\_user\]

</td><td>

Create, view, update, and delete the Feedback entities.

</td><td>

-   pf\_read
-   pf\_basic

</td></tr><tr><td>

\[sn\_align\_core.pf\_basic\]

</td><td>

Create, view, update, and delete the Feedback but cannot access the Feedback from Strategic Planning Workspace.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_wfs_qkr_zzb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Feedback

 \[sn\_align\_core\_feedback\]

</td><td>

Stores all the information about Feedback received from different sources.

</td></tr><tr><td>

Product idea

 \[sn\_align\_core\_product\_idea\]

</td><td>

Stores all the information about product ideas.

</td></tr><tr><td>

Feedback relationship

 \[sn\_align\_core\_m2m\_feedback\_rel\]

</td><td>

Stores information about the feedback associated to an entity \(planning or non-planning items\).

</td></tr></tbody>
</table>## System properties installed

<table id="table_jqk_wkr_zzb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_apw\_advanced.feedback.idea\_feedback\_queue\_address

</td><td>

Specifies the address for creating or submitting the feedback. With the **sn\_apw\_advanced.feedback.idea\_feedback\_queue\_address** system property, you can configure email settings within your instance and submit feedback directly from your email account.

</td></tr><tr><td>

sn\_apw\_advanced.product\_feedback\_allowed\_non\_planning\_items\_for\_link\_item

</td><td>

Specifies the non-planning items that can be linked to feedback or product idea. With the **sn\_apw\_advanced.product\_feedback\_allowed\_non\_planning\_items\_for\_link\_item** system property, you can link non-planning items such as incident, scrum tasks, agile stories, or items from safe application, agile development, PPM standard, or any global or scoped application tables to your feedback or product idea.

</td></tr><tr><td>

sn\_apw\_advanced.product\_feedback\_feedback\_filters

</td><td>

Specifies filters to sort through feedback information. With the **sn\_apw\_advanced.product\_feedback\_feedback\_filters** system property, you can configure to add and remove the filters on the feedback overview page.

</td></tr><tr><td>

sn\_apw\_advanced.product\_feedback\_product\_idea\_filters

</td><td>

Specifies filters to sort through product idea information. With the **sn\_apw\_advanced.product\_feedback\_product\_idea\_filters** system property, you can configure to add or remove the filters on the product idea overview page.

</td></tr><tr><td>

sn\_apw\_advanced.pf\_docs\_config

</td><td>

With the **sn\_apw\_advanced.pf\_docs\_config**, you can customize the Doc component using different attributes.-   Type: string
-   Possible value: JSON with key-value pair with these attributes:

    ```
{
    "hideLeftPanel": true/false,
    "hideDocTitle": false,
    "hideFavorites": false,
    "collapseLeftPanel": false,
    "collapseRigthPanel": false,
    "allowExternalLink": false,
    "implicitSave": true,
    "recordMentionEnabled": true,
    "userMentionEnabled": true,
    "recordMentionConfig": [{ (Record mention configuration)
        "sourceTable": TABLE_NAME,
        "filterCondition": "",
        "label": TABLE_LABEL,
        "fields": [
            FIELD1_NAME,
            FIELD2_NAME
        ]
    }],
}
    ```

-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_align\_ws.pf\_max\_list\_items

</td><td>

Specifies the maximum number of records displayed in the feedback or product idea list view. With the **sn\_align\_ws.pf\_max\_list\_items**, you can customize the feedback or product idea list view by setting a limit for the number of records displayed.-   Type: integer
-   Possible value: Any integer number greater than zero.
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>For more information on components installed with Strategic Planning, see [Components installed with Strategic Planning Workspace](../../alignment-planner-workspace/reference/components-installed-with-alignment-planner-workspace.md).

**Parent Topic:**[Feedback reference](product-feedback-reference.md)

