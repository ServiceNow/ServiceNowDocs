---
title: Software EOL request fields
description: Use the Software EOL request form to create a software end of life \(EOL\) request for software products in your asset estate that are reaching or have reached EOL.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Software EOL request fields

Use the Software EOL request form to create a software end of life \(EOL\) request for software products in your asset estate that are reaching or have reached EOL.

## Software EOL request form

<table id="table_rhj_z4k_3bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

A unique identifier for the EOL request.

</td></tr><tr><td>

Company

</td><td>

Name of the publisher of the software product.

</td></tr><tr><td>

Product

</td><td>

Name of the software product.

</td></tr><tr><td>

Edition

</td><td>

Edition of the software.

</td></tr><tr><td>

Version

</td><td>

Licensable version of the software.

</td></tr><tr><td>

Full version

</td><td>

The granular licensable version of the software.

</td></tr><tr><td>

Justification

</td><td>

Reason for starting the EOL request on the software.

</td></tr><tr><td>

Stage

</td><td>

The stage of the software EOL request. The default stage is **Draft**. Possible values include:-   Draft
-   Open
-   Analysis
-   Action initiated
-   Completed
-   Cancelled

</td></tr><tr><td>

Action initiated

</td><td>

The action taken to manage EOL risk. Possible values include:-   Pending
-   Remove EOL software
-   Upgrade
-   Purchase support
-   Move to Azure
-   Accept risk

</td></tr><tr><td>

Version type

</td><td>

Version type values include:-   Version \(build version\)
-   Full version \(main version\)

**Note:** You can manage EOL risk either for a version or full version of a software product.

</td></tr><tr><td>

Priority

</td><td>

Priority of the software EOL request.

</td></tr><tr><td>

Assignment group

</td><td>

The group from which an individual is selected to complete the software EOL request.

</td></tr><tr><td>

Assignment to

</td><td>

The individual assigned to complete the software EOL request, who is selected from the **Assignment group**.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the task.

</td></tr><tr><td>

Description

</td><td>

A detailed description of the task.

</td></tr><tr><td>

Work notes

</td><td>

Information about how the EOL workflow task is resolved.

</td></tr></tbody>
</table>## Software EOL tasks tab

<table id="table_ipf_rc1_4bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

A unique identifier for the software EOL task.

</td></tr><tr><td>

Name

</td><td>

Name of the software EOL task.

</td></tr><tr><td>

Software EOL request

</td><td>

The identifier of the software EOL request.

</td></tr><tr><td>

Parent

</td><td>

The identifier of the parent task.

</td></tr><tr><td>

State

</td><td>

The state of the software EOL task. The default state is **Open**.

</td></tr><tr><td>

Action

</td><td>

Indicates the action that you can take after deciding an IT strategy. Possible values include:-   Remove EOL software: Remove the EOL software product from the asset inventory.
-   Upgrade: Upgrade to the latest or the supported software version.
-   Purchase support: Purchase additional support for maintenance.
-   Move to Azure: Migrate to Microsoft Azure. This action is available only for Microsoft products.
-   Accept risk: Accept risks associated with the EOL software.

This field appears only when the value selected in the **Name** field is **Decide on IT strategy**.

</td></tr><tr><td>

Priority

</td><td>

Priority of the software EOL task.

</td></tr><tr><td>

Assignment group

</td><td>

The group from which an individual is selected to complete the software EOL task.

</td></tr><tr><td>

Assigned to

</td><td>

The individual assigned to complete the software EOL task, who is selected from the **Assignment group**.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the task.

</td></tr><tr><td>

Description

</td><td>

A detailed description of the task.

</td></tr><tr><td>

Notes

</td><td>

Additional information about the EOL task.

</td></tr><tr><td>

Work notes

</td><td>

Information about how the software EOL task is resolved.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

