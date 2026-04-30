---
title: Exploring Financial Services Operations Integration with Socure
description: Financial Services integration with Socure enables you to embed the Socure APIs in workflows and streamline your risk analysis processes.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Socure, Integrate, Financial Services Operations \(FSO\)]
---

# Exploring Financial Services Operations Integration with Socure

Financial Services integration with Socure enables you to embed the Socure APIs in workflows and streamline your risk analysis processes.

## Architectural Overview

The following diagram provides a high-level overview where you can see the design of the Socure integration and the role that each layer plays in Financial Services Operations \(FSO\).

![Diagrams of Know Your Customer, Socure integration for FSO, ServiceNow Integration Hub spoke, and Socure Native APIs. For the text description, refer to the Layers in the Socure integration section.](../image/fso_socure_integration_overview.png "Financial Services Operations Integration with Socure overview")

<table id="table_nwm_zkl_15b"><thead><tr><th>

Layer

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Spoke Layer

</td><td>

Layer that contains the Socure spoke plugin. This layer provides actions that use REST APIs to interact with Socure.

</td></tr><tr><td>

Adapter/Middle Layer

</td><td>

Layer that contains the Financial Services Operations application. This layer provides:-   Subflows that consume the actions in the Socure spoke. Each action has both individual subflows and combined subflows to call all the actions together.
-   A scheduled flow that obtains the latest **Reason Codes** and descriptions from Socure.

**Note:** When you are using Socure for the first time, you must activate the scheduled flow and set the desired frequency.


</td></tr><tr><td>

FSO Layer

</td><td>

Layer that contains the existing Financial Services Know Your Customer service. Additional tables and service definitions are added to this service to store customer-related identity verification data that is returned by Socure.The service definitions are as follows:

-   Socure-CDD–Customer
-   Socure-CDD–Contact

</td></tr></tbody>
</table>