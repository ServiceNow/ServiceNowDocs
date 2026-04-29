---
title: Read-only and client script modifiable fields in Asset Management tables
description: Comprehensive reference of Asset Management table fields that are restricted from UI editing and those which can be modified using client scripts.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Read-only fields in Asset Management, Client script modifiable fields in Asset Management, Asset Management, Asset Management tables]
breadcrumb: [Reference, Asset Management, IT Asset Management]
---

# Read-only and client script modifiable fields in Asset Management tables

Comprehensive reference of Asset Management table fields that are restricted from UI editing and those which can be modified using client scripts.

## Strict read-only fields in Asset Management tables

<table id="table_nyc_vsz_g3c"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Asset

 alm\_asset

</td><td>

-   Active transfer order \[active\_to\]
-   Configuration Item \[ci\]
-   Depreciated amount \[depreciated\_amount\]
-   Model component \[model\_component\_id\]
-   Old status \[old\_status\]
-   Old substatus \[old\_substatus\]
-   Pre-allocated \[pre\_allocated\]
-   Product instance identifier \[product\_instance\_id\]
-   Residual value \[residual\]
-   Residual date \[residual\_date\]
-   skip\_sync

</td></tr><tr><td>

Asset Creation Queue

 \[alm\_asset\_creation\_queue\]

</td><td>

-   Comments \[comments\]
-   Source ID \[source\_id\]
-   Table \[table\]

</td></tr><tr><td>

Consumable

 \[alm\_consumable\]

</td><td>

Planned for disposal \[planned\_for\_disposal\]

</td></tr><tr><td>

alm\_domain\_asset\_process\_setting

</td><td>

-   Active \[active\]
-   Domain \[sys\_domain\]

</td></tr><tr><td>

Fixed Assets

 \[alm\_fixed\_assets\]

</td><td>

-   Residual Value \[residual\]
-   Total cost \[total\_cost\]
-   Total depreciation \[total\_depreciation\]

</td></tr><tr><td>

Hardware

 \[alm\_hardware\]

</td><td>

Eligible for refresh \[eligible\_for\_refresh\]

</td></tr><tr><td>

Template Task

 \[alm\_template\_task\]

</td><td>

Class \[sys\_class\_name\]

</td></tr><tr><td>

Transfer Order

 \[alm\_transfer\_order\]

</td><td>

-   Number \[number\]
-   Requested date \[requested\_date\]
-   Return from \[return\_from\_transfer\_order\]
-   Stage \[stage\]
-   Type \[type\]

</td></tr><tr><td>

Transfer Order Line

 \[alm\_transfer\_order\_line\]

</td><td>

-   Number \[number\]
-   Quantity calculated \[quantity\_calculated\]
-   Quantity received \[quantity\_received\]
-   Quantity remaining \[quantity\_remaining\]
-   Quantity returned \[quantity\_returned\]
-   Stage \[stage\]
-   Transfer\_order \[transfer\_order\]

</td></tr><tr><td>

Transfer Order Line Subtask

 \[alm\_transfer\_order\_line\_subtask\]

</td><td>

-   Subtask name \[subtask\_name\]
-   Task \[task\]

</td></tr><tr><td>

Transfer Order Line Task

 \[alm\_transfer\_order\_line\_task\]

</td><td>

-   Model category \[model\_category\]
-   Stage \[stage\]
-   Template task \[template\_task\]
-   Transfer order line \[transfer\_order\_line\]

</td></tr><tr><td>

Content Audit

 \[asset\_content\_audit\]

</td><td>

-   Comments \[comments\]
-   Document key \[document\_key\]
-   Field name \[field\_name\]
-   New internal value \[new\_internal\_value\]
-   New value \[new\_value\]
-   Old Internal value \[old\_internal\_value\]
-   Old value \[old\_value\]
-   Class \[sys\_class\_name\]
-   Table name \[table\_name\]

</td></tr><tr><td>

Asset Job Log

 \[asset\_job\_log\]

</td><td>

Number \[number\]

</td></tr><tr><td>

Asset Job Log Details

 \[asset\_job\_log\_detail\]

</td><td>

-   Asset job log \[asset\_job\_log\]
-   Number \[number\]

</td></tr><tr><td>

Asset Reclamation Request

 \[asset\_reclamation\_request\]

</td><td>

-   Flow context \[flow\_context\]
-   Number \[number\]
-   State \[state\]

</td></tr><tr><td>

Contract

 \[ast\_contract\]

</td><td>

-   Approval History \[approval\_history\]
-   license\_quantity\_entitled
-   number
-   process
-   Has rate card \[ratecard\]
-   State \[state\]
-   Terms and conditions \[terms\_and\_conditions\]

</td></tr><tr><td>

Condition

 \[clm\_condition\_checker\]

</td><td>

table

</td></tr><tr><td>

Contract History

 \[clm\_contract\_history\]

</td><td>

-   Ends \[ends\]
-   Starts \[starts\]
-   Terms and Conditions \[terms\_and\_conditions\]

</td></tr><tr><td>

Asset Covered

 \[clm\_m2m\_rate\_card\_asset\]

</td><td>

Rate Card \[rate\_card\]

</td></tr><tr><td>

Terms and Conditions

 \[clm\_terms\_and\_conditions\]

</td><td>

-   Contract \[contract\]
-   Number \[number\]
-   Used \[used\]

</td></tr><tr><td>

Product Model

 \[cmdb\_model\]

</td><td>

-   Main component \[main\_component\]
-   Catalog Item \[product\_catalog\_item\]

</td></tr><tr><td>

Model Category

 \[cmdb\_model\_category\]

</td><td>

Bundle \[bundle\]

</td></tr><tr><td>

Model Lifecycle

 \[cmdb\_model\_lifecycle\]

</td><td>

-   Current lifecycle phase \[current\_lifecycle\_phase\]
-   Source \[source\]
-   Class \[sys\_class\_name\]

</td></tr><tr><td>

ITAM Licensing Resource Counts

 \[itam\_licensing\_resource\_counts\]

</td><td>

-   Active Subscription Entitlement \[active\_subscription\_entitlement\]
-   Is Aggregated \[is\_aggregated\]

</td></tr><tr><td>

Vendor Catalog Item

 \[pc\_vendor\_cat\_item\]

</td><td>

Product Catalog Item \[product\_catalog\_item\]

</td></tr><tr><td>

Purchase Order

 \[proc\_po\]

</td><td>

-   Initial request \[init\_request\]
-   Number \[number\]
-   Ordered \[ordered\]
-   Purchase order type \[purchase\_order\_type\]
-   Received \[received\]
-   Source ID \[source\_id\]
-   Source table \[source\_table\]
-   Status \[status\]
-   Total cost \[total\_cost\]

</td></tr><tr><td>

Purchase order line items

 \[proc\_po\_item\]

</td><td>

-   Number \[number\]
-   Ordered \[ordered\]
-   Purchase order \[purchase\_order\]
-   Received \[received\]
-   source\_id \[Source ID\]
-   Source table \[source\_table\]
-   Status \[status\]
-   Stock order \[stock\_order\]
-   total\_list\_price

</td></tr><tr><td>

Receiving Slip

 \[proc\_rec\_slip\]

</td><td>

-   Number \[number\]
-   Received \[received\]

</td></tr><tr><td>

Receiving Slip Line

 \[proc\_rec\_slip\_item\]

</td><td>

-   Number \[number\]
-   Received \[received\]
-   Receiving Slip \[receiving\_slip\]

</td></tr><tr><td>

Important Action Card

 \[sn\_itam\_recomm\_action\_card\]

</td><td>

Source \[source\]

</td></tr><tr><td>

Important Actions Dashboard Result

 sn\_itam\_recomm\_dashboard\_result

</td><td>

-   Dashboard \[dashboard\]
-   Last calculated on \[last\_calculated\_on\]
-   Schedule item \[schedule\_item\]
-   Domain \[sys\_domain\]

</td></tr><tr><td>

Important Actions Setup

 sn\_itam\_recomm\_setup

</td><td>

Source \[source\]

</td></tr><tr><td>

Important Actions Setup Result

 \[sn\_itam\_recomm\_setup\_result\]

</td><td>

-   Important action setup \[action\_setup\]
-   Active \[active\]
-   Duration \[duration\]
-   Last calculated on \[last\_calculated\_on\]
-   Query result \[query\_result\]
-   Domain \[sys\_domain\]

</td></tr><tr><td>

Important Actions Workspace

 \[sn\_itam\_recomm\_workspace\]

</td><td>

Results deletion in progress \[results\_deletion\_in\_progress\]

</td></tr><tr><td>

Zero Touch Refresh Fulfillment Request

 sn\_itam\_ztr\_fulfillment\_req

</td><td>

-   Customer request number \[customer\_request\_number\]
-   Number \[number\]

</td></tr></tbody>
</table>## Client script modifiable fields in Asset Management tables

<table id="table_y2l_nnq_h3c"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Transfer Order

 \[alm\_transfer\_order\]

</td><td>

-   From location \[from\_location\]
-   To location \[to\_location\]

</td></tr><tr><td>

Contract

 ast\_contract

</td><td>

Substate \[substate\]

</td></tr><tr><td>

Purchase order line items

 proc\_po\_item

</td><td>

Total cost \[total\_cost\]

</td></tr></tbody>
</table>