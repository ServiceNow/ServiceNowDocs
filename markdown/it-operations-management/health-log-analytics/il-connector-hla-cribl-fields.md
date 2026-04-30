---
title: Cribl integration configuration fields
description: Description of the fields on the Cribl integration configuration forms for Health Log Analytics.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Cribl integration configuration fields

Description of the fields on the Cribl integration configuration forms for Health Log Analytics.

For the Cribl integration setup procedure, see [Set up a Cribl integration for Health Log Analytics](../task/il-connector-hla-cribl.md).

<table id="table_ogk_rh4_jfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My Cribl integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

Service Instance

</td><td>

The service instance \(formerly the application service\) to which to bind the log data. This field is required.

</td></tr><tr><td>

MID Server name

</td><td>

The MID Server to which the Cribl logs are streamed. This field is required.

</td></tr><tr><td>

Port

</td><td>

The port on the MID Server. This field is required.Choose a port within the range 6000-6200 from the array. The port must not be occupied by another process. Make sure that your organization’s security team opens the selected port on the MID Server.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr><tr><td>

Transport \(for push integrations\)

</td><td>

The protocol used for streaming log messages to your ServiceNow instance: TCP. This field is read-only.

</td></tr><tr><td>

Source \(for pull integrations\)

</td><td>

The source of the log data that the integration pulls to your ServiceNow instance: Cribl. This field is read-only.

</td></tr></tbody>
</table><table id="table_wk2_nn4_jfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cribl URL

</td><td>

The URL of the Cribl instance. This field is required.HLA uses this URL to establish the connection with the Cribl instance and make the necessary API calls.

For example:

-   On-Prem: https://my-cribl.company.com:9000
-   Cloud: https://myorg-12345abcde.cribl.cloud
-   Sandbox: https://sandbox-xyz789.sandbox.cribl.io

</td></tr><tr><td>

Authentication method

</td><td>

The authentication method used by the Cribl integration. This field is required. The Cribl integration supports:

-   Token-based authentication: Required for Cribl Cloud and also supported for self-hosted \(On-Prem\) Cribl instances.
-   Basic authentication: Preferred for self-hosted \(On-Prem\) Cribl instances.

Both of these authentication methods use the default credential alias: Cribl\_Credential\_Alias.

For information about setting up credentials for the authentication method used by the Cribl integration, see [Set up authentication credentials for the Cribl integration in Health Log Analytics](../task/hla-setup-cribl-credentials.md).

**Important:** Verify that only one active credential record of each credentials type exists under the credential alias.

</td></tr><tr><td>

Worker Group

</td><td>

The Cribl Worker Group from which to stream log data to the instance. This field is required.The drop-down list displays Worker Groups based on the provided Cribl cloud instance URL and authentication method.

For example:

-   default
-   dev-workers
-   prod-workers
-   staging-workers

</td></tr><tr><td>

Cribl route

</td><td>

The Cribl route that directs log data to a specific destination.This field is auto-populated with a drop-down list of all available routes, each configured with a default destination. Select the desired route from the list. This field is required.

For example:

-   default
-   demo-route

</td></tr><tr><td>

Cribl destination

</td><td>

The Cribl destination to which the log data is directed. This field is auto-populated and read-only.When HLA populates this field, it provides a link to the destination on the Cribl server.

For example: sn\_hla\_cribl\_tcp\_json\_abcdef

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration field descriptions](../concept/hla-connector-config-fields.md)

