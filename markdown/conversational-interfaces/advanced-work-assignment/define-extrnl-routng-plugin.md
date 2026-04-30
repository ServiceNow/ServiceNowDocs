---
title: Define external routing test implementation
description: Define the External Routing Test Tools plugin \[com.glide.awa.external.test\_tools\] with a simplified external-routing-provider sample Automated Test Framework \(ATF\) by using the demo data that is available with the plugin installation.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Define external routing test implementation

Define the External Routing Test Tools plugin \[com.glide.awa.external.test\_tools\] with a simplified external-routing-provider sample Automated Test Framework \(ATF\) by using the demo data that is available with the plugin installation.

To run the ExternalRoutingConfigurationTestTool, verify that you have:

-   Loaded the demo data for AWA, awa.external, and awa.external.test\_tools.
-   Filled up the credentials in the **AutomationUser** in the sys\_auth\_profile\_basic table.
-   Created the HTTP\(s\) Connection in sys\_alias, ServiceNow\_Basic record.

You must open the ExternalRoutingConfigurationTestTool record and click Run Test to complete the actions of the External Routing test.

## Functions of the External Routing Test Tools plugin \(com.glide.awa.external.test\_tools\)

When the External Routing Test Tools plugin \(com.glide.awa.external.test\_tools\) is run, it validates if:

-   The Connection record is created in the HTTP\(S\) Connection \[http\_connection\].
-   The Credentials are provided in the HTTP\(S\) Connection \[http\_connection\].
-   The AWA\_Queue record is updated successfully with the following values:
    -   **External** = **true**
    -   **Provider** = **ServiceNow Demo**
-   A record is successfully created in the Interaction \[interaction\] table with the following values:
    -   **Short description** = **Created from ATF test automation**
    -   **State** = **New**
    -   **Type** = **Chat**
-   The record is automatically created in the Work Item.
-   The Server-Side Validation Script is run by passing the Work Item ID to the Workflow Studio and calling to the external third-party CCaaS provider.
-   The sys\_flow\_context ID is retrieved from the sys\_flow\_context execution.
-   The retrieved sys\_flow\_context ID provides the payload response.
-   The payload response belongs to the Work Item that you have created.
-   The Server-Side Validation Script is run to verify if the response is successful and then the payload is sent to the Manual Assignment REST API.
-   The authorization for credentials is configured in the Basic Auth Configuration \[sys\_auth\_profile\_basic\] table.
-   An Agent is available in the User \[sys\_user\] table to ascend the payload.
-   The Server-Side Validation Script is run to confirm that the Agent is available in the correct Service Channel.
-   The Manual Assignment REST API is called when the Agent is available.
-   The response status is successful and the response payload contains `Manual Assignment successfully requested`.
-   The AWA Work Item is successfully assigned to the Agent and is not in the queue state.

    **Note:** If the test fails at any step, the detailed information about where the configuration failed is provided to the user along with the solution to fix it.


**Parent Topic:**[Configuring Advanced Work Assignment](../task/installing-awa.md)

