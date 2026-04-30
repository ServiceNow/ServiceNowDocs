---
title: Legal Tracker Outside Counsel Engagement request form
description: Fields in the Legal Tracker Outside Counsel Engagement request form of a legal matter.
locale: en-US
release: yokohama
product: Legal Matter Management
classification: legal-matter-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Legal Matter Management reference, Legal Matter Management, Legal Service Delivery, Employee Service Management]
---

# Legal Tracker Outside Counsel Engagement request form

Fields in the Legal Tracker Outside Counsel Engagement request form of a legal matter.

Refer to the table for the fields on Outside Counsel Engagement form and how they are mapped when we integrate to create a matter in Legal Tracker.

|Field|Description|Mapped parameters in Legal Tracker Matters API|
|-----|-----------|----------------------------------------------|
|Request Details|
|Requested for|Name of the user requesting for the Outside Counsel.|None|
|OCE Number|Unique identifier of the Outside Counsel record.|None|
|Reason for engaging an Outside Counsel|Description of the reasons for recruitment of Outside Counsel.|None|
|Describe the scope of work to be performed|Description of the scope of work to be performed by the outside counsel.|None|
|Firm Details|
|Firm Access|Option to define the firm access to the matter from the drop-down list.|firmAccess|
|Lead firm|Main firm with which the Outside Counsel is associated.|None|
|Lead Outside Counsel|Lead counsel of the associated Lead firm.|None|
|Matter Details|
|Full matter name/Parties Involved|Full name of the matter or the parties to be associated with the outside counsel.|fullNameAndPartiesInvolved|
|Short matter name|Short name of the matter to be associated with the outside counsel.|shortName|
|Lead company person|Lead of the organization who should coordinate with the outside counsel.|leadCompanyPersonEmail|
|\#2 company person|Alternative contact person in the absence of the Lead company person.|numberTwoCompanyPersonEmail|
|Matter description|Detailed description of the matter.|description|
|Start date|Start date for the Outside Counsel. This date must be ahead of today's date.|startDate|
|Fee arrangement|Type of fees to be selected from the drop-down list.|leadFirmFeeArrangement|
|Amount|Amount to be provided to the outside counsel according to the fee arrangement.|None|
|Legal Tracker Details|
|Create a task for entering Legal Tracker field details|Option to select to create a legal matter task and delegate the task to fill in the Legal Tracker Details section. For more information, see [Request Outside Counsel engagement](../task/create-lt-outside-counsel-engagement.md).|None|
|Matter group|Associated matter group of the Outside Counsel record.|matterGroup|
|Matter type|Associated matter type of the Outside Counsel record.|matterType|
|Associated matter ID|Associated matter ID of the Outside Counsel.|associatedMatterId|
|Country|Country of operation of the outside counsel.|countryOrRegion|
|Practice group|Associated practice group of the outside counsel.|practiceGroup|
|Organizational unit|Associated organizational unit of the outside counsel.|organizationalUnit|
|Substantive law|Associated substantive law of the outside counsel.|substantiveLaw|
|Invoice approval route|Associated invoice approval route of the outside counsel.|invoiceApprovalRoute|
|AP route|Associated accounts payable route of the outside counsel.|apRoute|

**Parent Topic:**[Legal Matter Management reference](../../legal-matter-management/reference/legal-matter-management-reference.md)

