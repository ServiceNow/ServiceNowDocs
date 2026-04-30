---
title: Cribl data input configuration fields
description: Description of the fields on the Cribl data input configuration form.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Cribl data input configuration fields

Description of the fields on the Cribl data input configuration form.

<table id="table_uwp_g5n_sdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data input name

</td><td>

Name of the new data input. This field is required.

</td></tr><tr><td>

Description

</td><td>

Description of the data input.

</td></tr><tr><td>

MID server

</td><td>

The MID Server to which the Cribl logs are streamed.This field is required.

</td></tr><tr><td>

Port

</td><td>

The port on the MID Server.

Choose a port within the suggested range from the array. The port must not be occupied by another process. Make sure that your organization’s security team opens the selected port.

This field is required.

</td></tr></tbody>
</table><table id="table_wjp_m5n_sdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cribl instance URL

</td><td>

The URL of the Cribl instance. HLA uses this URL to establish the connection with the Cribl instance.

</td></tr><tr><td>

Cribl API token

</td><td>

The Cribl API token HLA uses to authenticate with Cribl and make API calls.

</td></tr></tbody>
</table><table id="table_xxk_r5n_sdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cribl route

</td><td>

The Cribl route that directs log data to a specific destination.This field is auto-populated with a drop-down list of all available routes, each configured with a default destination. You must select the desired route from this list. This field is required.

</td></tr><tr><td>

Cribl destination

</td><td>

The created Cribl destination. The Cribl destination points to the MID Server host and port configured in the data input. This field is read-only.

</td></tr></tbody>
</table>**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

