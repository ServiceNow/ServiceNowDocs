---
title: Execute RFC in the Source-to-Pay with SAP integration
description: Execute RFC from the available list.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-23"
reading_time_minutes: 1
breadcrumb: [Exploring Source-to-Pay integration with SAP ECC and S4HANA, Source-to-Pay integration with SAP ECC and SAP S4 HANA, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Execute RFC in the Source-to-Pay with SAP integration

Execute RFC from the available list.

**Process flow**:

Step 1 - Create a record for SAP system in Connection and Credential alias table.

Step 2 - Create Credential for connecting to SAP system.

Step 3 - Add Mid server and credentials to the connection.

Step 4 - Create ERP Source is ERP source configuration table.

Step 5 - Create Service, add flow and give the necessary inputs in the fields.

![Figure 0-1: Flow chart illustrating RFC Execution.](../image/rfc-execution.png)

**Name**: ZSN\_BAPI\_GET\_DATA

<table id="table_owl_24z_lxb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

Input

</td></tr><tr><td>

1

</td><td>

Connection Alias -

</td><td>

Connection Alias for SAP ECC – RFC

</td></tr><tr><td>

2

</td><td>

RFC

</td><td>

The Reference to records \(SAP RFC Name and Application Component\) in SAP RFC Table

</td></tr><tr><td>

3

</td><td>

Input

</td><td>

Input fields for the selected RFC, represented in a flat structure

</td></tr><tr><td class="sub-head" colspan="3">

Output

</td></tr><tr><td>

1

</td><td>

Response

</td><td>

The response for the execution of selected RFC in SAP

</td></tr><tr><td>

2

</td><td>

Action Status

</td><td>

If the request is executed successfully, Status is set to “Success”. If there is a failure in SAP ECC - RFC, Status is set to “Error"

</td></tr><tr><td>

3

</td><td>

Error Message

</td><td>

Reason for error. Populated only when an error occurs. Error returned from SAP in the RETURN parameter.No or empty response received from SAP

</td></tr></tbody>
</table>-   Error! Reference source not found.

    ![Function Builder Initial Screen](../../sourcing-procurement-operations/image/function-builder-initial-screen.png "Function Builder Initial Screen")

-   Error! Reference source not found.Error! Reference source not found.

    ![IMPORT, CHANGING, and TABLES parameters](../../sourcing-procurement-operations/image/test-function-module.png "Enter the IMPORT, CHANGING, and TABLES parameters")

-   ![Results data](../../sourcing-procurement-operations/image/test-function-module-result-screen.png "Results data")

-   Error! Reference source not found

    ![Results data](../../sourcing-procurement-operations/image/structure-editor.png "Results data")

    ![Results Data](../../sourcing-procurement-operations/image/structure-editor-display-it.png "Results data")


