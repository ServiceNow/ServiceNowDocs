---
title: Define a service contract
description: A new table of SLA contracts is provided through the Service Level Management Service Contracts module. These contracts group together SLAs that relate to a single vendor or customer, as well as the CIs, locations, groups, users, and child contracts that are related to the contract.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Service Level Management, Service Level Management, IT Service Management]
---

# Define a service contract

A new table of SLA contracts is provided through the **Service Level Management** &gt; **Service Contracts** module. These contracts group together SLAs that relate to a single vendor or customer, as well as the CIs, locations, groups, users, and child contracts that are related to the contract.

The table Service Contract \[ast\_service\] extends the table Contract \[ast\_contract\]. It stores information about service contracts for asset management purposes. To get the service contract functionality, activate the Service Level Management - Contract Management Integration \[com.snc.sla.contract2\] plugin. Installing the SLA Contract Add-on plugin adds relations to this table to make it useful for Service Management purposes. Once the plugin is installed, the Service Contract record possesses related lists for:

-   SLAs
-   Contract CIs
-   Contract Locations
-   Contract Groups
-   Contract Users
-   Child Contracts

<table id="table_ly1_sdr_bbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

A unique number associated with the contract.

</td></tr><tr><td>

Starts

</td><td>

The date on which the contract takes effect.

</td></tr><tr><td>

Ends

</td><td>

The date on which the contract expires.

</td></tr><tr><td>

Approver

</td><td>

The person who approves the contract.

</td></tr><tr><td>

Location

</td><td>

The primary location of the contract, if applicable. If there are multiple, use the Contract locations related list.

</td></tr><tr><td>

Active

</td><td>

Whether the contract is currently in use.

</td></tr><tr><td>

Automatically renew/extend

</td><td>

Whether the contract has the possibility of being renewed or extended at the end of its term.

</td></tr><tr><td>

Vendor

</td><td>

The vendor responsible for the contract.

</td></tr><tr><td>

Vendor account

</td><td>

The account the vendor is responsible to.

</td></tr><tr><td>

Contract number

</td><td>

The number of the contract defining the Service Contract.

</td></tr><tr><td>

Total cost

</td><td>

The total cost of the contract.

</td></tr><tr><td>

Payment amount

</td><td>

The amount which has been paid so far.

</td></tr><tr><td>

Payment schedule

</td><td>

The duration at which payments are made.

</td></tr><tr><td>

Process non-contractual SLAs

</td><td>

If selected, you can have both contractual SLAs as well as non-contractual SLAs, such as OLA and Underpinning contracts, processed for the same task. You can track the contractual SLAs as well as any SLA that is internal to the organization to enhance compliance.

**Note:** The **Process non-contractual SLAs** check box is available for the zboot and upgrade customers. The system property **com.snc.sla.contract.tables** is not available for zboot customers so that contracts are processed for any table in the system instead of specific tables.

</td></tr><tr><td>

Short description

</td><td>

A short description of the Service Contract.

</td></tr><tr><td>

Description

</td><td>

A full description of the Service Contract.

</td></tr></tbody>
</table>## Add contract field to task form

Depending on how the contract is used, the **Contract** field can be added to any task form by configuring the form. For information about how to configure a form, see [Form configuration](https://www.servicenow.com/docs/access?context=basic-form-administration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) . As the **Caller**, **Assignment Group**, **Location**, and **Configuration item** fields are populated, the **Contract** field filters appropriately, helping the support desk to associate the ticket to the correct contract.

**Note:** Do not add the same field to different sections of a form unless the field displays read-only data. Having two or more instances of an editable field can cause data loss and prevent the proper functioning of UI and data policies.

**Parent Topic:**[Exploring Service Level Management](exploring-slm.md)

