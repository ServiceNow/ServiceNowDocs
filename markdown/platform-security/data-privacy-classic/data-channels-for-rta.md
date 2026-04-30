---
title: Data channels for real-time anonymization policies
description: Select the data channel for use with real time anonymization\(RTA\).
locale: en-US
release: yokohama
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: reference
last_updated: "2025-03-28"
reading_time_minutes: 1
breadcrumb: [Real time anonymization, Data privacy \(Store\), Data Privacy, Platform Privacy]
---

# Data channels for real-time anonymization policies

Select the data channel for use with real time anonymization\(RTA\).

A data channel is the channel taken by your data for processing. You can control which channel RTA discovered data is sent to when [configuring an anonymization policy](../task/dps-create-anonymization-policies.md). The following are the data channels available for use with RTA:

<table id="table_zk1_2nc_v2c"><thead><tr><th>

Channel

</th><th>

Description

</th><th>

Techniques and Patterns supported

</th><th>

Role required

</th></tr></thead><tbody><tr><td>

Now Assist

</td><td>

Masks sensitive data within prompts and responses.

</td><td>

-   Regular expressions
-   Synthetic data replacement

</td><td>

now\_assist\_data\_privacy\_admin

</td></tr><tr><td>

Data Extraction

</td><td>

Scrub sensitive data from data shared with ServiceNow to improve our AI systems.**Note:** Only available to customers with data sharing enabled. Data sharing is on by default.

</td><td>

-   Regular expressions
-   Synthetic data replacement

</td><td>

now\_assist\_data\_privacy\_admin

</td></tr><tr><td>

Data Kit

</td><td>

The Now Assist Data Kit plugin for Now Assist enables you to add datasets to a data catalog and create collections for use in ServiceNow SDK.

</td><td>

-   Regular expressions
-   Named entity recognition\(NER\)
-   Synthetic data replacement

</td><td>

data\_kit\_data\_privacy\_admin

</td></tr></tbody>
</table>