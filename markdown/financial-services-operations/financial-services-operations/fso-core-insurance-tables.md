---
title: FSO Core Insurance tables
description: This section explains the insurance tables in FSO Core and how they handle insurance data.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-09-23"
reading_time_minutes: 2
---

# FSO Core Insurance tables

This section explains the insurance tables in FSO Core and how they handle insurance data.

## Insurance tables installed

|Label|Table name|Description|
|-----|----------|-----------|
|Business Owners Policy|sn\_bom\_bo\_ins\_policy|Insurance Policy|
|Claim Base|sn\_bom\_claim\_base|Claim base is the table from which all the insurance app specific claim case types are extended. This table contains all the common attributes which can be used across insurance claims case types.|
|Commercial Auto Policy|sn\_bom\_ca\_ins\_policy|Insurance commercial auto policy table extended from insurance policy.|
|Commercial Property Policy|sn\_bom\_cp\_ins\_policy|Insurance commercial property policy table extended from insurance policy.|
|Commercial Umbrella Policy|sn\_bom\_cu\_ins\_policy|Insurance commercial umbrella policy table extended from insurance policy.|
|Condo Policy|sn\_bom\_condo\_ins\_policy|Insurance personal condo policy table extended from insurance policy.|
|Farm Ranch Policy|sn\_bom\_fr\_ins\_policy|Insurance commercial farm ranch policy table extended from insurance policy.|
|General Liability Policy|sn\_bom\_gl\_ins\_policy|Insurance general liability policy table extended from insurance policy.|
|Group Disability Insurance Policy|sn\_bom\_group\_disability\_ins\_policy|Insurance group disability policy table extended from insurance policy.|
|Group Life Insurance Policy|sn\_bom\_group\_life\_ins\_policy|Insurance group life policy table extended from insurance policy.|
|Homeowner Policy|sn\_bom\_homeowner\_ins\_policy|Insurance homeowners policy table extended from insurance policy.|
|Individual Disability Policy|sn\_bom\_indiv\_disab\_policy|Insurance individual disability policy table extended from insurance policy.|
|Individual Life Policy|sn\_bom\_indiv\_life\_policy|Insurance individual life policy table extended from insurance policy.|
|Insurance Policy|sn\_bom\_ins\_policy|Stores all insurance policy account records. Extends the Sold Product \[sn\_install\_base\_sold\_product\] table.|
|Insured Property|sn\_bom\_insured\_property|Insured property table references customer property and will contain the properties of a customer which are covered by an insurance policy.|
|Landlord Policy|sn\_bom\_landlord\_ins\_policy|Insurance landlord policy table extended from insurance policy.|
|Personal Auto Policy|sn\_bom\_auto\_ins\_policy|Insurance personal auto policy table extended from insurance policy.|
|Personal Umbrella Policy|sn\_bom\_pu\_ins\_policy|Insurance personal umbrella policy table extended of insurance policy.|
|Policy Coverage|sn\_bom\_policy\_coverage|Policy coverage table will contain the defined coverages on the insurance policy.|
|Policy Participant|sn\_bom\_policy\_participant|Policy participant table will contain the defined participants on the insurance policy.|
|Policy Participant Role|sn\_bom\_policy\_participant\_insured\_property|Policy participant role table will contain the roles played by the participants who have been defined on the insurance policy.|
|Renters Policy|sn\_bom\_renters\_ins\_policy|Insurance personal renters policy table extended from insurance policy.|
|Transaction|sn\_bom\_ins\_policy\_transaction|Stores all policy transaction records. Extends the Financial Transaction \[sn\_bom\_transaction\] table.|

**Parent Topic:**[Financial Services Operations Core](financial-services-operations-core-data-model.md)

