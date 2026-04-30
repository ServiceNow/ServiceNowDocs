---
title: Export intelligence system properties
description: This section describes the record limitations and its properties while exporting data.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-04-15"
reading_time_minutes: 1
breadcrumb: [Working with Data Exports, Use, Threat Intelligence Security Center, Security Operations]
---

# Export intelligence system properties

This section describes the record limitations and its properties while exporting data.

**Note:** TISC provides the following limit for data exports. To set the following properties, navigate to **System Properties** &gt; **Import Export**.

Role required: sn\_sec\_tisc.export

<table id="table_ygb_vht_dfc"><thead><tr><th>

Format

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

STIX 2.1 JSON

</td><td>

sn\_sec\_tisc.stix\_export\_limit

</td><td>

Maximum number of rows that can be exported to a STIX 2.1 file.The default e is 10000.

</td></tr><tr><td>

STIX 2.1 JSON

</td><td>

sn\_sec\_tisc.stix\_export\_payload\_streaming\_attachment\_min\_objects\_size

</td><td>

If the count of objects in "Objects" array of STIX export payload is greater than the number specified in this property then JSONStreamingAPI will be used for creating attachment.The default export limit is 4000.

</td></tr><tr><td>

STIX 2.1 JSON

</td><td>

sn\_sec\_tisc.stix\_json\_from\_json\_streaming\_api\_action\_timeout

</td><td>

Timeout\(in seconds\) that will be used when triggering flow designer action for generating STIX JSON attachment using JSON streaming API.The default export limit is 900.

</td></tr></tbody>
</table>**Note:** For better understanding of export limit on the other format types, see [Export limits](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/exporting-data/concept/c_ExportLimits.html).

