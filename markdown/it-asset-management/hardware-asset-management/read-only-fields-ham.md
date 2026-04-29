---
title: Read-only and client script modifiable fields in HAM tables
description: Comprehensive reference of HAM table fields that are restricted from UI editing and those which can be modified using client scripts.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Read-only fields in Hardware Asset Management, Client script modifiable fields in Hardware Asset Management, Hardware Asset Management, Hardware Asset Management tables]
breadcrumb: [Hardware Asset Management reference, Hardware Asset Management, IT Asset Management]
---

# Read-only and client script modifiable fields in HAM tables

Comprehensive reference of HAM table fields that are restricted from UI editing and those which can be modified using client scripts.

## Strict read-only fields in HAM tables

<table id="table_nyc_vsz_g3c"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Asset

 \[alm\_asset\]

</td><td>

-   Audit number \[audit\_number\]
-   Audit type \[audit\_type\]
-   Audited by \[audited\_by\]
-   Disposal order number \[disposal\_order\_number\]
-   Last audit date \[last\_audit\_date\]
-   Last audit state \[last\_audit\_state\]
-   Process ID \[process\_id\]
-   Process table \[process\_table\]
-   Refresh request line \[refresh\_request\_line\]
-   Attestation number \[attestation\_number\]
-   Attested by \[attested\_by\]
-   Last attestation date \[last\_attestation\_date\]
-   Last attestation state \[last\_attestation\_state\]
-   Disposal order number \[sn\_itam\_common\_disposal\_order\_number\]

</td></tr><tr><td>

Asset Covered

 \[clm\_m2m\_contract\_asset\]

</td><td>

-   Flow context \[flow\_context\]
-   Extension contract \[lease\_extension\_contract\]
-   Purchase order line \[po\_line\_item\]
-   Stage \[stage\]

</td></tr><tr><td>

Consumable Model Lifecycle

 \[cmdb\_consumable\_model\_lifecycle\]

</td><td>

Content active \[content\_active\_status\]

</td></tr><tr><td>

Consumable Model

 \[cmdb\_consumable\_product\_model\]

</td><td>

-   License opt in \[norm\_license\_opt\_in\]
-   Normalization combination \[normalized\_combination\]
-   Normalized date \[normalized\_date\]
-   Normalization hash 1 \[normalized\_hash1\]
-   Normalization hash 2 \[normalized\_hash2\]
-   Normalization hash 3 \[normalized\_hash3\]
-   Normalization hash 4 \[normalized\_hash4\]
-   Normalization rule \[normalized\_rule\]
-   Normalized rule table \[normalized\_rule\_table\]
-   Normalization status \[normalized\_status\]
-   Normalization status summary \[normalized\_status\_summary\]

</td></tr><tr><td>

Hardware Model Lifecycle

 \[cmdb\_hardware\_model\_lifecycle\]

</td><td>

Content active \[content\_active\_status\]

</td></tr><tr><td>

Hardware Model

 \[cmdb\_hardware\_product\_model\]

</td><td>

-   License opt in \[norm\_license\_opt\_in\]
-   Normalization combination \[normalized\_combination\]
-   Normalized date \[normalized\_date\]
-   Normalization hash 1 \[normalized\_hash1\]
-   Normalization hash 2 \[normalized\_hash2\]
-   Normalization hash 3 \[normalized\_hash3\]
-   Normalization hash 4 \[normalized\_hash4\]
-   Normalization rule \[normalized\_rule\]
-   Normalized rule table \[normalized\_rule\_table\]
-   Normalization status \[normalized\_status\]
-   Normalization status summary \[normalized\_status\_summary\]

</td></tr><tr><td>

Product Model

 \[cmdb\_model\]

</td><td>

-   Norm Status Sumry Function \[norm\_status\_sumry\_function\]
-   TRM product phase \[trm\_product\_phase\]

</td></tr><tr><td>

Model Category

 \[cmdb\_model\_category\]

</td><td>

Resource category \[resource\_category\]

</td></tr><tr><td>

Asset Audits

 \[sn\_hamp\_asset\_audit\]

</td><td>

-   Audit number \[audit\_number\]
-   Excluded from HAM \[excluded\]
-   Scanned and expected \[expected\]
-   New \[new\]
-   Scanned and not expected \[not\_expected\]
-   Expected and not found \[not\_found\]
-   Scan date \[scan\_date\]
-   Status \[status\]

</td></tr><tr><td>

Hardware Asset Reclamation Line

 \[sn\_hamp\_asset\_reclaim\_line\]

</td><td>

-   Asset \[asset\]
-   Asset reclamation request \[asset\_reclaim\_request\]
-   Flow context \[flow\_context\]
-   Number \[number\]
-   Stage \[stage\]

</td></tr><tr><td>

Hardware Asset Reclamation Task

 \[sn\_hamp\_asset\_reclaim\_task\]

</td><td>

-   Hardware asset reclamation line \[asset\_reclaim\_line\]
-   Start date \[start\_date\]
-   Task name \[task\_name\]

</td></tr><tr><td>

Asset RMA Task

 \[sn\_hamp\_asset\_rma\_task\]

</td><td>

-   RMA request line \[rma\_request\_line\]
-   Task name \[task\_name\]

</td></tr><tr><td>

Hardware Disposal Order

 \[sn\_hamp\_hardware\_disposal\]

</td><td>

-   Number \[number\]
-   Stage \[stage\]

</td></tr><tr><td>

Hardware Disposal Tasks

 \[sn\_hamp\_hw\_asset\_disposal\_task\]

</td><td>

-   Departed \[departed\_assets\]
-   Expected \[expected\_assets\]
-   Not departed \[not\_departed\_assets\]
-   Not verified \[not\_verified\_assets\]
-   Substate \[substate\]
-   Task name \[task\_name\]
-   Verified \[verified\_assets\]

</td></tr><tr><td>

Device Type

 \[sn\_hamp\_hw\_device\_type\]

</td><td>

-   Stage active \[stage\_active\]
-   Stage description \[stage\_description\]
-   Stage name \[stage\_name\]
-   Stage UNSPSC commodity ID \[stage\_unspsc\_commodity\_id\]
-   Class \[sys\_class\_name\]

</td></tr><tr><td>

Hardware Manufacturer

 \[sn\_hamp\_hw\_manufacturer\]

</td><td>

-   Name \[name\]
-   Stage active \[stage\_active\]
-   Stage description \[stage\_description\]
-   Stage name \[stage\_name\]
-   Stage webpage \[stage\_webpage\]
-   Class \[sys\_class\_name\]
-   Webpage \[webpage\]

</td></tr><tr><td>

Hardware Normalization Map

 \[sn\_hamp\_hw\_normalization\_map\]

</td><td>

-   Hash \[hash\]
-   Product \[hw\_product\]
-   Product model \[hw\_product\_model\]
-   Class \[sys\_class\_name\]

</td></tr><tr><td>

Hardware Product

 \[sn\_hamp\_hw\_product\]

</td><td>

-   Stage active \[stage\_active\]
-   Stage description \[stage\_description\]
-   Stage device type \[stage\_device\_type\]
-   Stage manufacturer \[stage\_hw\_manufacturer\]
-   Stage name \[stage\_name\]
-   Class \[sys\_class\_name\]

</td></tr><tr><td>

Hardware Model Library

 \[sn\_hamp\_hw\_product\_model\]

</td><td>

-   Stage active \[stage\_active\]
-   Stage description \[stage\_description\]
-   Stage product \[stage\_hw\_product\]
-   Stage model number \[stage\_model\_number\]
-   Stage name \[stage\_name\]
-   Class \[sys\_class\_name\]

</td></tr><tr><td>

Hardware Asset Refresh Line

 \[sn\_hamp\_hw\_refresh\_line\]

</td><td>

-   Flow context \[flow\_context\]
-   Number \[number\]
-   Replacement model \[replacement\_model\]
-   Request item \[request\_item\]
-   Stage \[stage\]

</td></tr><tr><td>

Refresh Line Tasks

 \[sn\_hamp\_hw\_refresh\_line\_task\]

</td><td>

Replacement model \[replacement\_model\]

</td></tr><tr><td>

HAMP Import File

 \[sn\_hamp\_import\_file\]

</td><td>

-   Details \[details\]
-   File name \[file\_name\]
-   Status \[status\]

</td></tr><tr><td>

Hardware Lifecycle Definition

 \[sn\_hamp\_lifecycle\_definition\]

</td><td>

-   Product model \[hw\_product\_model\]
-   Lifecycle code \[lifecycle\_code\]
-   Lifecycle phase \[lifecycle\_phase\]
-   Phase start date \[start\_date\]
-   Class \[sys\_class\_name\]

</td></tr><tr><td>

Loaner Asset Order

 \[sn\_hamp\_loaner\_asset\_order\]

</td><td>

-   Asset Prepared \[asset\_prepared\]
-   Flow context \[flow\_context\]
-   Justification \[justification\]
-   Lead Time \[lead\_time\]
-   Loaner order status \[loaner\_order\_status\]
-   Preparation start date \[preparation\_start\_date\]
-   Request type \[request\_type\]
-   Return Date \[return\_date\]
-   Stage \[stage\]
-   Start Date \[start\_date\]

</td></tr><tr><td>

Audits to Scanned Assets

 \[sn\_hamp\_m2m\_audit\_asset\]

</td><td>

-   Asset \[asset\]
-   Asset audit \[asset\_audit\]
-   Audit status \[audit\_status\]

</td></tr><tr><td>

Planned Assets

 \[sn\_hamp\_m2m\_hw\_asset\_disposal\]

</td><td>

-   Scanned \[depart\_scanned\]
-   Hardware disposal order \[hardware\_disposal\]
-   Stage \[stage\]
-   Scanned \[verify\_scanned\]

</td></tr><tr><td>

Replacement Models

 \[sn\_hamp\_m2m\_ztr\_replacement\_model\]

</td><td>

Zero touch refresh model \[refresh\_model\]

</td></tr><tr><td>

Manage Hardware Library

 \[sn\_hamp\_manage\_hw\_library\]

</td><td>

Status \[status\]

</td></tr><tr><td>

HAM Maturity Content

 \[sn\_hamp\_maturity\_content\]

</td><td>

-   Staging type \[stage\_type\]
-   Type \[type\]

</td></tr><tr><td>

HAM Maturity Item

 \[sn\_hamp\_maturity\_item\]

</td><td>

Type \[type\]

</td></tr><tr><td>

Model Category Normalization Summary

 \[sn\_hamp\_model\_ctg\_norm\_summary\]

</td><td>

Model category \[model\_category\]

</td></tr><tr><td>

sn\_hamp\_provider\_task\_mapping

</td><td>

Status \[status\]

</td></tr><tr><td>

HAM Resource Category

 \[sn\_hamp\_resource\_category\]

</td><td>

-   Opt in \[opt\_in\]
-   Resource Category \[resource\_category\]
-   Schedule item \[schedule\_item\]
-   Subscription unit ratio \[su\_ratio\]

</td></tr><tr><td>

RMA Request

 \[sn\_hamp\_rma\_request\]

</td><td>

-   Flow context \[flow\_context\]
-   Number \[number\]
-   Stage \[stage\]
-   State \[state\]

</td></tr><tr><td>

RMA Request Line

 \[sn\_hamp\_rma\_request\_line\]

</td><td>

-   Asset \[asset\]
-   Flow context \[flow\_context\]
-   Model \[model\]
-   Number \[number\]
-   Quantity \[quantity\]
-   RMA request \[rma\_request\]
-   Stage \[stage\]

</td></tr><tr><td>

Zero touch request task

 \[sn\_hamp\_zero\_touch\_request\_task\]

</td><td>

-   Number \[number\]
-   Task name \[task\_name\]
-   Zero touch request \[zero\_touch\_request\]

</td></tr><tr><td>

Zero Touch Refresh Request

 \[sn\_hamp\_ztr\_request\]

</td><td>

-   Asset \[asset\]
-   City \[city\]
-   Country \[country\]
-   Email address \[email\]
-   Zero touch refresh fulfillment request \[fulfillment\_request\]
-   Mobile number \[mobile\]
-   Name \[name\]
-   Number \[number\]
-   Order state \[order\_state\]
-   Provider \[provider\]
-   Refresh method \[refresh\_method\]
-   Replacement model \[replacement\_model\]
-   Requested for \[requested\_for\]
-   Return stockroom \[return\_stockroom\]
-   RMA request \[rma\_request\]
-   Stage \[stage\]
-   State \[state\]
-   State/Province \[state\_loc\]
-   Street \[street\]
-   Zip/Postal code \[zip\]

</td></tr><tr><td>

Zero Touch Refresh Task

 \[sn\_hamp\_ztr\_task\]

</td><td>

-   Number \[number\]
-   Substate \[substate\]
-   task name \[task\_name\]
-   Zero touch refresh request \[zero\_touch\_req\]

</td></tr><tr><td>

Zero Touch Refresh Fulfillment Request

 \[sn\_itam\_ztr\_fulfillment\_req\]

</td><td>

Provider \[provider\]

</td></tr><tr><td>

Pallet

 \[alm\_pallet\]

</td><td>

Number \[pallet\_number\]

</td></tr><tr><td>

Transfer Order Line Task

 \[alm\_transfer\_order\_line\_task\]

</td><td>

Substate \[substate\]

</td></tr><tr><td>

Asset Task

 \[asset\_task\]

</td><td>

DaaS account \[daas\_account\]

</td></tr><tr><td>

Contract

 \[ast\_contract\]

</td><td>

-   Flow context \[cmn\_flow\_context\]
-   Process ID \[process\_id\]
-   Process table \[process\_table\]
-   Substate \[substate\]

</td></tr><tr><td>

Contract History

 \[clm\_contract\_history\]

</td><td>

-   Previous contract ends \[previous\_contract\_ends\]
-   Previous contract Id \[previous\_contract\_id\]
-   Previous contract starts \[previous\_contract\_starts\]
-   Renewal date \[renewal\_date\]

</td></tr><tr><td>

Model Lifecycle

 \[cmdb\_model\_lifecycle\]

</td><td>

-   Lifecycle code \[lifecycle\_code\]
-   Source \[source\]

</td></tr><tr><td>

itam\_aia\_log

</td><td>

-   AI agent feature \[aia\_feature\]
-   Number \[number\]
-   Source \[source\]
-   Source table \[source\_table\]
-   Domain \[sys\_domain\]
-   User \[user\]

</td></tr><tr><td>

Purchase Order

 \[proc\_po\]

</td><td>

-   Purchase order type \[purchase\_order\_type\]
-   Source ID \[source\_id\]
-   Source table \[source\_table\]
-   PO type \[po\_type\]

</td></tr><tr><td>

Purchase order line items

 \[proc\_po\_item\]

</td><td>

-   Source ID \[source\_id\]
-   Source table \[source\_table\]

</td></tr><tr><td>

Contract Renewal Request

 \[sn\_contract\_renewal\_request\]

</td><td>

-   Approval \[approval\]
-   Approval history \[approval\_history\]
-   Contract \[contract\]
-   Flow context \[flow\_context\]
-   Number \[number\]
-   Stage \[stage\]
-   State \[state\]

</td></tr><tr><td>

Contract Renewal Request Line

 \[sn\_contract\_renewal\_request\_line\]

</td><td>

-   Contract \[contract\]
-   Contract administrator \[contract\_administrator\]
-   Applicable taxes \[contract\_applicable\_taxes\]
-   Contract approver \[contract\_approver\]
-   End date \[contract\_ends\]
-   Invoice payment terms \[contract\_invoice\_payment\_terms\]
-   Payment amount \[contract\_payment\_amount\]
-   Payment schedule \[contract\_payment\_schedule\]
-   Options \[contract\_renewal\_options\]
-   Contract renewal request \[contract\_renewal\_request\]
-   Name \[contract\_short\_description\]
-   Start date \[contract\_starts\]
-   Tax cost \[contract\_tax\_cost\]
-   Effective tax rate\[contract\_tax\_rate\]
-   Total cost \[contract\_total\_cost\]
-   Flow context \[flow\_context\]
-   Number \[number\]
-   Renewal contract \[renewal\_contract\]
-   Stage \[stage\]
-   State \[state\]
-   Contract number \[vendor\_contract\]

</td></tr><tr><td>

Contract Renewal Task

 \[sn\_contract\_renewal\_task\]

</td><td>

-   Contract renewal request \[contract\_renewal\_request\]
-   Contract renewal request line \[contract\_renewal\_request\_line\]
-   Renewal approver \[renewal\_approver\]
-   Renewal contract \[renewal\_contract\]
-   Task name \[task\_name\]

</td></tr><tr><td>

sn\_daas\_common\_rma\_response\_orderline

</td><td>

-   Flow context \[flow\_context\]
-   Shipment order \[shipment\_order\]
-   Stage \[stage\]

</td></tr><tr><td>

Carrier Integration Profile

 \[sn\_itam\_carrier\_int\_profile\]

</td><td>

Job \[job\]

</td></tr><tr><td>

Import asset data rows

 \[sn\_itam\_cmn\_import\_asset\_row\]

</td><td>

-   Asset \[asset\_id\]
-   Model \[model\_id\]
-   Status \[status\]

</td></tr><tr><td>

Asset attestation

 \[sn\_itam\_common\_asset\_attestation\]

</td><td>

-   Attestation number \[attestation\_number\]
-   Requested by \[requested\_by\]
-   Schedule \[schedule\]
-   Submission date \[submission\_date\]
-   Domain \[sys\_domain\]
-   Table \[table\]

</td></tr><tr><td>

Asset Audits

 \[sn\_itam\_common\_asset\_audit\]

</td><td>

Audit number \[audit\_number\]

</td></tr><tr><td>

Asset remediation task

 \[sn\_itam\_common\_asset\_rmdt\_task\]

</td><td>

Task name \[task\_name\]

</td></tr><tr><td>

Asset Warranty

 \[sn\_itam\_common\_asset\_warranty\]

</td><td>

-   Active \[active\]
-   Asset \[asset\]
-   Country \[country\]
-   Description \[description\]
-   End date \[end\_date\]
-   External warranty ID \[external\_warranty\_id\]
-   Name \[name\]
-   Start date \[start\_date\]
-   Status \[status\]
-   Type \[type\]

</td></tr><tr><td>

Attestations for asset

 \[sn\_itam\_common\_attestation\_asset\_m2m\]

</td><td>

-   Asset \[asset\]
-   Asset attestation \[attestation\]
-   Attestation date \[attestation\_date\]
-   Domain \[sys\_domain\]
-   User \[user\]

</td></tr><tr><td>

Asset attestation schedule

 \[sn\_itam\_common\_attestation\_schedule\]

</td><td>

-   Requested by \[requested\_by\]
-   Schedule number \[schedule\_number\]
-   Domain \[sys\_domain\]
-   Table \[table\]

</td></tr><tr><td>

Calculated Lifecycle formula

 \[sn\_itam\_common\_calc\_lc\_formula\]

</td><td>

Name \[name\]

</td></tr><tr><td>

Asset Donation Order

 \[sn\_itam\_common\_donation\_order\]

</td><td>

-   Number \[number\]
-   Stage \[stage\]

</td></tr><tr><td>

Asset Donation Task

 \[sn\_itam\_common\_donation\_task\]

</td><td>

-   Departed \[departed\_assets\]
-   Expected \[expected\_assets\]
-   Not departed \[not\_departed\_assets\]
-   Substate \[substate\]
-   Task name \[task\_name\]

</td></tr><tr><td>

sn\_itam\_common\_inbound\_asset\_order

</td><td>

-   Source order \[source\_order\]
-   Source order table \[source\_order\_table\]

</td></tr><tr><td>

sn\_itam\_common\_inbound\_asset\_orderline

</td><td>

-   Flow context \[flow\_context\]
-   Shipment order \[shipment\_order\]
-   Stage \[stage\]

</td></tr><tr><td>

Lifecycle Code

 \[sn\_itam\_common\_lifecycle\_code\]

</td><td>

-   Code \[code\]
-   Long description \[long\_description\]
-   Short description \[short\_description\]

</td></tr><tr><td>

Planned Assets

 \[sn\_itam\_common\_m2m\_ast\_donation\]

</td><td>

-   Asset donation order \[asset\_donation\_order\]
-   Stage \[stage\]

</td></tr><tr><td>

Shipment line

 \[sn\_itam\_common\_m2m\_shipment\_asset\]

</td><td>

-   Alert \[alert\]
-   Stage \[asset\_stage\]

</td></tr><tr><td>

Stockroom Distribution Channel

 \[sn\_itam\_common\_m2m\_stockroom\_channel\]

</td><td>

Function \[function\]

</td></tr><tr><td>

Asset prepare task

 \[sn\_itam\_common\_prepare\_task\]

</td><td>

Task name \[task\_name\]

</td></tr><tr><td>

Asset put away task \[sn\_itam\_common\_put\_away\_task\]

</td><td>

Task name \[task\_name\]

</td></tr><tr><td>

Import asset data

 \[sn\_itam\_common\_receive\_import\]

</td><td>

-   Number of rows with errors \[rows\_errors\]
-   Number of rows processed \[rows\_processed\]
-   Number of rows ready to be received \[rows\_ready\]
-   Number of rows successful \[rows\_successful\]
-   Status \[status\]

</td></tr><tr><td>

Schedule task

 \[sn\_itam\_common\_schedule\_task\]

</td><td>

Task name \[task\_name\]

</td></tr><tr><td>

Asset selection task

 \[sn\_itam\_common\_selection\_task\]

</td><td>

Task name \[task\_name\]

</td></tr><tr><td>

Asset ship task

 \[sn\_itam\_common\_ship\_task\]

</td><td>

-   Shipment order \[shipment\_order\]
-   Task name \[task\_name\]

</td></tr><tr><td>

Shipment

 \[sn\_itam\_common\_shipment\]

</td><td>

-   Shipment number \[shipment\_number\]
-   Stage \[stage\]
-   Shipment quantity \[shipment\_quantity\]

</td></tr><tr><td>

Shipping Carrier

 \[sn\_itam\_common\_shipping\_carrier\]

</td><td>

Profile mapped date \[profile\_mapped\_date\]

</td></tr><tr><td>

Renewal contracts

 \[sn\_m2m\_renewal\_contract\]

</td><td>

Renewal task \[renewal\_task\]

</td></tr></tbody>
</table>## Client script modifiable fields in HAM tables

<table id="table_sy3_sqq_h3c"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Hardware

 alm\_hardware

</td><td>

Failure risk score \[risk\_score\]

</td></tr></tbody>
</table>**Parent Topic:**[Hardware Asset Management reference](../concept/reference-hardware-asset-management.md)

