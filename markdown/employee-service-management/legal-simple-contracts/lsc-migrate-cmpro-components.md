---
title: Data copied to Contract Management Pro for Legal Service Delivery during migration from Legal Simple Contracts
description: A migration utility copies data from Legal Simple Contracts tables to Contract Management Pro for Legal Service Delivery tables.
locale: en-US
release: xanadu
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Migrate to Contract Management Pro for Legal Service Delivery from Legal Simple Contracts, Migrating to Contract Management Pro for Legal Service Delivery, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Data copied to Contract Management Pro for Legal Service Delivery during migration from Legal Simple Contracts

A migration utility copies data from Legal Simple Contracts tables to Contract Management Pro for Legal Service Delivery tables.

<table id="table_mfq_4kl_zyb"><thead><tr><th>

Legal Simple Contracts tables

</th><th>

Contract Management Pro for Legal Service Delivery tables

</th></tr></thead><tbody><tr><td>

Contract type\[sn\_lg\_contracts\_type\]

</td><td>

Contract type \[sn\_cm\_core\_contract\_type\]

</td></tr><tr><td>

Legal Contract \[sn\_lg\_contracts\_repository\]

</td><td>

Legal Contracts Repository\[sn\_lg\_cnt\_repository\]

</td></tr></tbody>
</table>## Contract type table

The contract type table is copied to Contract Management Pro for Legal Service Delivery.

If a contract type already exists in the Contract Management Pro for Legal Service Delivery table, the contract type is not migrated.

After migration, any modification or deletion of the contract type in the Legal Simple Contracts table will not be automatically synced to the Contract Management Pro for Legal Service Delivery table.

<table id="table_hj4_kjl_zyb"><thead><tr><th>

Contract type \[sn\_lg\_contracts\_type\]

</th><th>

Contract type \[sn\_cm\_core\_contract\_type\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name

</td><td>

Name of the contract type.

</td></tr><tr><td>

Active

</td><td>

Active

</td><td>

State of the contract type.

</td></tr><tr><td>

Domain

</td><td>

Domain

</td><td>

Regional domain.

</td></tr></tbody>
</table>## Legal Contract Repository table

Legal requests for non-disclosure agreement and third-party contract reviews that are in the Close Complete state are copied to Contract Management Pro for Legal Service Delivery

The following table provides the details of the Legal Simple Contracts data and the corresponding Contract Management Pro for Legal Service Delivery data.

<table id="table_contract_request_form"><thead><tr><th>

Legal Contract \[sn\_lg\_contracts\_repository\]

</th><th>

Legal Contracts Repository\[sn\_lg\_cnt\_repository\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract Request

</td><td>

Contract Request

</td><td>

Contract request number

</td></tr><tr><td>

Contract Status

</td><td>

State

</td><td>

The state of the request. The mapping between states in the old and new repository.

-   Terminated in the old repository is marked as Cancelled in the new repository.
-   If the start date of the contract is in the past, Amended in the old repository is marked as Active.
-   If the start date of the contract is in the future, Amended in the old repository is marked as Draft.
-   Expired in the old table without dates is marked as Expired in the new table.
-   Expired in the old table with contract start date in the past is marked as Active.
-   Expired in the old table with a contract end date in past is marked as expired.
-   Expired in the old table with a contract start date in future is marked as Draft.
-   Active in the old table with a start date in past is marked as Active.
-   Active in the old table with a start date in the future is marked as Draft.
-   Active in the old table without dates is marked as Active.
-   Canceled in the old repository is marked as Canceled in the new repository.

</td></tr><tr><td>

Number

</td><td>

Legacy Contract

</td><td>

The contract number from Legal Simple Contracts.

</td></tr><tr><td>

Contract Type

</td><td>

Contract Type

</td><td>

Type of contract from Contract Management Pro for Legal Service Delivery table.

</td></tr><tr><td>

Contract Start Date

</td><td>

Starts

</td><td>

Start date of contract

</td></tr><tr><td>

Contract End Date

</td><td>

Ends

</td><td>

End date of contract

</td></tr><tr><td>

Contract Owner

</td><td>

Contract administrator

</td><td>

The administrator of the contract.

</td></tr><tr><td rowspan="2">

Company Name

</td><td>

Company Legal name

</td><td rowspan="2">

The Vendor field is populated based on the availability of Company Name in the Companies \[core\_company\] table.-   Company name exists.
    -   Single match found - Vendor is populated with the company name.
    -   Multiple matches found - Vendor field is populated with the Company Legal name. When the contract repository record is opened, a recommendation is displayed to modify the Vendor value manually.
-   New company does not exist in both tables.
    -   Single match found- Vendor is populated with the company name.
    -   Multiple matches found- Vendor field is not populated and an error is displayed when the record is opened. You can map the value for Vendor manually.

When there is no match for vendor field, the company name is copied to company legal name and error is displayed to fill the vendor value.


</td></tr><tr><td>

Vendor

</td></tr><tr><td>

Company Address

</td><td>

None

</td><td>

The Company Address is part of the Vendor details.

</td></tr><tr><td>

Country

</td><td>

None

</td><td>

The Country details are part of the Vendor details.

</td></tr><tr><td>

None

</td><td>

Contract type model

</td><td>

Contract model associated with the contract type.

</td></tr></tbody>
</table><table id="table_hcb_mvl_zyb"><thead><tr><th>

Legal Contract \[sn\_lg\_contracts\_repository\]

</th><th>

Contract Document\[sn\_cm\_core\_document\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

None

</td><td>

Name

</td><td>

Name of the document. The name is in the format "&lt;contract type&gt; for &lt;company\_name&gt;." If the contract type is empty, the name is in the format "&lt;contract\_number&gt; for &lt;company\_name&gt;."

</td></tr><tr><td>

External folder URL

</td><td>

URL

</td><td>

URL of the external storage folder.

</td></tr><tr><td>

External folder id

</td><td>

External id

</td><td>

ID of the external storage folder.

</td></tr><tr><td>

External provider

</td><td>

Storage provider

</td><td>

Document storage provider.

</td></tr><tr><td>

Request opened by

</td><td>

Owner

</td><td>

The user who opened the request.

</td></tr><tr><td>

None

</td><td>

Contract type

</td><td>

Contract type corresponding to the record.

</td></tr><tr><td>

None

</td><td>

Default version

</td><td>

Version of the document revision that is marked as Ready.

</td></tr></tbody>
</table><table id="table_i3j_zvl_zyb"><thead><tr><th>

Legal Contract \[sn\_lg\_contracts\_repository\]

</th><th>

Contract Document Revision\[sn\_cm\_core\_document\_revision\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Refer to the newly created document

</td><td>

Document

</td><td>

Revision of the document.

</td></tr><tr><td>

None

</td><td>

Name

</td><td>

Name of the document revision.For external storage: The name is in the format "&lt;contract type&gt; for &lt;company\_name&gt;." If the contract type is empty, the name is in the format "&lt;contract\_number&gt; for &lt;company\_name&gt;."

For internal storage: The name is in the format &lt;document\_name&gt;.

</td></tr><tr><td>

None

</td><td>

File type

</td><td>

The type of document revision.For external storage, the document revision type is a URL.

For internal storage, the document revision type is an attachment.

</td></tr><tr><td>

Signed Contract

</td><td>

URL

</td><td>

The signed contract is available at the external storage URL.

</td></tr><tr><td>

External file ID

</td><td>

External id

</td><td>

ID of the external file.

</td></tr><tr><td>

None

</td><td>

Version state

</td><td>

The document revision number, which is set to 1 initially.

</td></tr><tr><td>

Document

</td><td>

Document

</td><td>

The file in the document field is copied to the newly created revision record.

</td></tr></tbody>
</table>**Parent Topic:**[Migrate to Contract Management Pro for Legal Service Delivery from Legal Simple Contracts](migration-to-cmpro.md)

