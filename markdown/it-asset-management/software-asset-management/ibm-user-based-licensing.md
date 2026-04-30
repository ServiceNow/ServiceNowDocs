---
title: IBM user-based licenses
description: You can use the Software Asset Management publisher pack for IBM to track and manage your IBM user-based licenses, including authorized user licenses and user value unit \(UVU\)-based licenses.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Supported IBM license types, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# IBM user-based licenses

You can use the Software Asset Management publisher pack for IBM to track and manage your IBM user-based licenses, including authorized user licenses and user value unit \(UVU\)-based licenses.

Supported UVU-based licenses include authorized UVU, employee UVU, and external UVU. The publisher pack adds license metrics that are specific to IBM so that you can calculate licensing for these license types.

IBM user-based licensing enables you to license the users who require access to your IBM software products. You can track and optimize the compliance of your IBM user-based licenses by reconciling the associated IBM software products through client access records. With a client access record, you can specify the total number of users who are granted access to a particular version of an IBM software product. For more granular control, you can also identify the specific users who are granted access to that product. The Software Asset Management application can then compare this information against the software rights and allocations that are defined in the corresponding software entitlements to determine if the associated user-based licenses are compliant.

For more information on client access records in the Software Asset Workspace, see [Create a software client access record in workspace](../task/create-clientaccess-workspace.md). For more information on client access records in the Software Asset Management classic application, see [Add a software client access record in Software Asset Management classic](../task/t_AddAClientAccessRec.md).

## Authorized user licensing

Authorized user licensing enables you to license each unique user who requires access to an IBM software product.

With this licensing type, you can install a given IBM software product on an unlimited number of configuration items \(CIs\), such as servers and computers. Each user can then access an unlimited number of installations for that software product on any of the CIs that the software product is installed on.

## Authorized user value unit \(AUVU\) licensing

Authorized user value unit \(AUVU\) licensing enables you to license the total number of unique users who require access to an IBM software product.

With this licensing type, you can install a given IBM software product on an unlimited number of configuration items \(CIs\), such as servers and computers. Each user can then access an unlimited number of installations for that software product on any of the CIs that the software product is installed on.

With AUVU licensing, the number of users who require access to an IBM software product corresponds directly with an AUVU tier number and factor value.

|Number of Users|Tier|Factor|
|---------------|----|------|
|1 to 20|1|1.00|
|21 to 50|2|0.83|
|51 or more|3|0.80|

You can determine the number of rights that are required for an AUVU license by using a step function based on these AUVU tiers. First, divide the total number of users into tiers based on the [AUVU tiers and factors table](ibm-user-based-licensing.md#table_owy_slv_4pb). Then, multiply the number of users within each tier by the corresponding factor values. Finally, add the resulting numbers together to determine the total number of rights that are required for the AUVU license.

**Important:** If you do not have enough rights to license all users, none of the users are licensed and the product is marked as Not Compliant.

For example, a company wants to grant 150 employees and contractors access to an IBM software product so that they can collaborate on an upcoming project. The total number of rights that are required for the corresponding AUVU license is 125, based on the following calculations:

<table id="table_zbt_s4z_2qb"><thead><tr><th>

Tier

</th><th>

Number of Users within the Tier

</th><th>

Factor

</th><th>

Number of Rights Required

</th></tr></thead><tbody><tr><td>

1 \(1 to 20 users\)

</td><td>

20

</td><td>

1.00

</td><td>

20 x 1.00 = 20

</td></tr><tr><td>

2 \(21 to 50 users\)

</td><td>

30

</td><td>

0.83

</td><td>

30 x 0.83 = 24.9

</td></tr><tr><td>

3\(51 or more users\)

</td><td>

100

</td><td>

0.80

</td><td>

100 x 0.8 = 80

</td></tr><tr><td>

—

</td><td>

150 total

</td><td>

—

</td><td>

20 + 24.9 + 80 = 124.9 total \(rounded up to 125 total\)

</td></tr></tbody>
</table>## Employee user value unit \(EUVU\) licensing

Employee user value unit \(EUVU\) licensing enables you to license the total number of users within your organization who require access to an IBM software product. These users can include both employees and contractors.

With EUVU licensing, the number of users who require access to an IBM software product corresponds directly with an EUVU tier number and factor value.

|Number of Users|Tier|Factor|
|---------------|----|------|
|1000 to 2,500|1|1.000|
|2,501 to 5,000|2|0.800|
|5,001 to 10,000|3|0.700|
|10,001 to 30,000|4|0.650|
|30,001 to 50,000|5|0.550|
|50,001 to 100,000|6|0.500|
|100,001 to 300,000|7|0.465|
|300,001 to 500,000|8|0.400|
|500,001 to 1,000,000|9|0.360|
|1,000,001 to 100,000,000|10|0.320|

You can determine the number of rights that are required for an EUVU license by using a step function based on these EUVU tiers. First, divide the total number of users into tiers based on the [EUVU tiers and factors table](ibm-user-based-licensing.md#table_gsg_z53_ftb). Then, multiply the number of users within each tier by the corresponding factor values. Finally, add the resulting numbers together to determine the total number of rights that are required for the EUVU license.

**Important:** If you do not have enough rights to license all users, none of the users are licensed and the product is marked as Not Compliant.

For example, a company wants to grant 11,000 employees access to an IBM software product. The total number of rights that are required for the corresponding EUVU license is 8,650, based on the following calculations:

<table id="table_hsg_z53_ftb"><thead><tr><th>

Tier

</th><th>

Number of Users within the Tier

</th><th>

Factor

</th><th>

Number of Rights Required

</th></tr></thead><tbody><tr><td>

1 \(1,000 to 2,500 users\)

</td><td>

2,500

</td><td>

1.000

</td><td>

2,500 x 1.000 = 2,500

</td></tr><tr><td>

2 \(2,501 to 5,000 users\)

</td><td>

2,500

</td><td>

0.800

</td><td>

2,500 x 0.800 = 2,000

</td></tr><tr><td>

3\(5,001 to 10,000 users\)

</td><td>

5,000

</td><td>

0.700

</td><td>

5,000 x 0.700 = 3,500

</td></tr><tr><td>

4\(10,001 to 30,000 users\)

</td><td>

1,000

</td><td>

0.650

</td><td>

1,000 x 0.650 = 650

</td></tr><tr><td>

—

</td><td>

11,000 total

</td><td>

—

</td><td>

2,500 + 2,000 + 3,500 + 650 = 8,650 total

</td></tr></tbody>
</table>## External user value unit \(XUVU\) licensing

External user value unit \(XUVU\) licensing enables you to license the total number of users outside your organization who require access to an IBM software product. These users can include third-party partners, suppliers, and contractors.

With XUVU licensing, the number of users who require access to an IBM software product corresponds directly with an XUVU tier number and factor value.

|Number of Users|Tier|Factor|
|---------------|----|------|
|1000 to 10,000|1|1.00000|
|10,001 to 50,000|2|0.87500|
|50,001 to 100,000|3|0.60000|
|100,001 to 500,000|4|0.43750|
|500,001 to 1,000,000|5|0.30000|
|1,000,001 to 25,000,000|6|0.24375|
|25,000,001 to 50,000,000|7|0.15000|
|50,000,001 to 250,000,000|8|0.13750|
|250,000,001 to 500,000,000|9|0.05000|
|500,000,001 to 100,000,000,000|10|0.05000|

You can determine the number of rights that are required for an XUVU license by using a step function based on these XUVU tiers. First, divide the total number of users into tiers based on the [XUVU tiers and factors table](ibm-user-based-licensing.md#table_ily_vw3_ftb). Then, multiply the number of users within each tier by the corresponding factor values. Finally, add the resulting numbers together to determine the total number of rights that are required for the XUVU license.

**Important:** If you do not have enough rights to license all users, none of the users are licensed and the product is marked as Not Compliant.

For example, a company wants to grant 15,000 third-party partners access to an IBM software product. The total number of rights that are required for the corresponding XUVU license is 14,375, based on the following calculations:

<table id="table_jly_vw3_ftb"><thead><tr><th>

Tier

</th><th>

Number of Users within the Tier

</th><th>

Factor

</th><th>

Number of Rights Required

</th></tr></thead><tbody><tr><td>

1 \(1,000 to 10,000 users\)

</td><td>

10,000

</td><td>

1.00000

</td><td>

10,000 x 1.00000 = 10,000

</td></tr><tr><td>

2\(10,001 to 50,000 users\)

</td><td>

5,000

</td><td>

0.87500

</td><td>

5,000 x 0.87500 = 4,375

</td></tr><tr><td>

—

</td><td>

15,000 total

</td><td>

—

</td><td>

10,000 + 4,357 = 14,375 total

</td></tr></tbody>
</table>**Parent Topic:**[Supported IBM license types](supported-ibm-license-types.md)

