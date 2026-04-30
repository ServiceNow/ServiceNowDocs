---
title: Setting up an insurance policy for Insurance claims
description: Learn how to set up an insurance policy by using the Insurance claims application. Each new type of insurance policy requires that you create a dedicated table for that specific insurance policy type.
locale: en-US
release: zurich
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up the policy data for Insurance claims, Configure, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Setting up an insurance policy for Insurance claims

Learn how to set up an insurance policy by using the Insurance claims application. Each new type of insurance policy requires that you create a dedicated table for that specific insurance policy type.

-   **[Insurance policies in Insurance claims](insurance-policies.md)**  
In Financial Services Operations, the Insurance Policy \(sn\_bom\_ins\_policy\) table is the base table for all insurance policies. Whenever a new type of policy is introduced in Insurance claims, you create a dedicated table for that insurance policy type.
-   **[Create an insurance policy table](../task/create-an-insurance-policy-table.md)**  
Create a table that extends the Insurance Policy \(sn\_bom\_ins\_policy\) table in the Insurance claims application. You use this table to hold all the information about insurance policies of a particular type that you sold to your customers. Creating tables helps to ensure that each type of policy is properly organized and maintained within the system.
-   **[Create a role to access insurance policy tables](../task/create-roles-acls-and-grant-access.md)**  
Create a role to enable an authorized agent to access tables that extend the Insurance Policy \(sn\_bom\_ins\_policy\) table by using the Insurance claims application. By creating a role, you ensure that only authorized agents can view the policies that are relevant to their roles.
-   **[Create an access control list for an insurance policy table](../task/create-an-access-control-list-for-the-insurance-policy-table.md)**  
Create an access control list \(ACL\) for a table that extends the Insurance Policy \(sn\_bom\_ins\_policy\) table by using the Insurance claims application. By creating an ACL, you ensure that users with specific roles can interact with tables for a particular insurance policy.
-   **[Grant the Insurance claims roles access to an insurance policy table](../task/grant-insurance-claims-roles-access-to-the-insurance-policy-table.md)**  
Grant the Insurance claims contributor \(sn\_ins\_gen\_claim.fnol\_representative\) and agent \(sn\_ins\_gen\_claim.processor\) roles with access to an insurance policy table by using the Insurance claims application. This way, the users with these roles can view the policy details when they’re processing claims.
-   **[Create an insurance policy](../task/create-an-insurance-policy-for-a-consumer.md)**  
Create a policy record in the system that represents the agreement between the insurance provider and the customer by using the Insurance claims application.
-   **[Apply coverages to an insurance policy](../task/apply-coverage-to-an-insurance-policy.md)**  
Define the coverages for an insurance policy by using the Insurance claims application. You can define what coverages types and coverage options apply to a customer's insurance policy.
-   **[Add a policy participant to an insurance policy](../task/add-a-policy-participant-to-an-insurance-policy.md)**  
Add a customer to an insurance policy as the insured entity by using the Insurance claims application.
-   **[Add a related list to an insurance product model](../task/add-related-list-to-insurance-product-model.md)**  
Add a related list of an insurance policy table to an insurance product model table by using the Insurance claims application. Adding a related list displays the customer insurance policies for a particular insurance product.

**Parent Topic:**[Setting up the policy data for Insurance claims](set-up-policy-data-for-insurance-claims.md)

**Related topics**  


[Insurance policies in Insurance claims](insurance-policies.md)

[Policy snapshots in Insurance claims](policy-snapshots.md)

