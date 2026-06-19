---
title: Execute RFC in the Source-to-Pay with SAP integration
description: Execute RFC from the available list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/execute-rfc-source-to-pay-sap-integration.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Execute RFC in the Source-to-Pay with SAP integration

Execute RFC from the available list.

**Process flow**:

Step 1 - Create a record for the SAP system in the Connection and Credential alias table.

Step 2 - Create Credential for connecting to the SAP system.

Step 3 - Add MID Server and credentials to the connection.

Step 4 - Create ERP Source is an ERP source configuration table.

Step 5 - Create a Service, add flow and give the necessary inputs in the fields.

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

The Reference to records \(SAP RFC Name and Application component\) in SAP RFC Table

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

The response for the execution of selected RFC at SAP

</td></tr><tr><td>

2

</td><td>

Action Status

</td><td>

If the request is executed successfully, Status is set to “Success”. If there’s a failure in SAP ECC - RFC, Status is set to “Error"

</td></tr><tr><td>

3

</td><td>

Error Message

</td><td>

Reason for error. Populated only when an error occurs. Error returned from SAP in the RETURN parameter.No or empty response received from SAP

</td></tr></tbody>
</table>-   \[Omitted image "function-builder-initial-screen.png"\] Alt text: Function Builder Initial Screen

-   \[Omitted image "test-function-module.png"\] Alt text: IMPORT, CHANGING, and TABLES parameters

-   \[Omitted image "test-function-module-result-screen.png"\] Alt text: Results data

-   \[Omitted image "structure-editor.png"\] Alt text: Results data

    \[Omitted image "structure-editor-display-it.png"\] Alt text: Results Data


