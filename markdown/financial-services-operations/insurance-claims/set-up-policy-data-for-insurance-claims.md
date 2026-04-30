---
title: Setting up the policy data for Insurance claims
description: Set up the policy data for the Insurance claims application by importing the policy data into your instance, or by using remote tables to reference the policy data.
locale: en-US
release: yokohama
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Setting up Insurance claims, Insurance claims, Claims applications, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Setting up the policy data for Insurance claims

Set up the policy data for the Insurance claims application by importing the policy data into your instance, or by using remote tables to reference the policy data.

## Importing the policy data

If you store your insurance policy data in an external system, you should bring in the latest insurance policies for all your customers from that system into your instance. Synchronize the latest insurance policies from the external system daily.

The base system, by default, uses the latest insurance policy records that are available. It generates a policy snapshot using this data during the claim creation process. For more information, see [Policy snapshots in Insurance claims](policy-snapshots.md).

You may bring in past policy coverages or any other past policy data if those policies apply on the incident date of a claim. If you want to create a claim against these policies, you must have the foundational claims data available to select the correct policy. For more information about the foundational claims data, see the next section.

## Foundational claims data

When you're bringing in policy coverages or any other policy components, you should import the following key information into your ServiceNow instance before you create any claims:

-   Insurance product models
-   Consumers
-   Accounts
-   Contacts
-   Basic insurance policy information, such as the following details:
    -   Policy holder
    -   Policy participants
    -   Effective dates
    -   Policy status

This foundational data is essential for ensuring that claims are created with accurate and up-to-date policy details. The insurance product model and basic policy information act as the backbone for claims processing, while coverages can be retrieved dynamically based on the incident date when necessary. This approach ensures flexibility without sacrificing critical information during claim creation.

## Using remote tables to search for policies

If you already have an existing policy management system, you can use an API and remote tables to search for policies when you’re selecting a policy during intake. When a policy is selected, you can create a policy record to associate the policy to the claim.

For more information about the remote data options or how to set up a remote table integration, see the following topics in the Developer Guide:

-   [Remote Data Options for Remote Tables](../../../integrate/guides/FSO/concept/fso-int_guide-remote-data-options-for-remote-tables.md)
-   [Setting up a remote table integration](../../../integrate/guides/FSO/concept/setting-up-a-remote-table-integration.md)

## Setting up the new policy data

For more information about defining the product models for your insurance products, defining the coverage specifications and options, or creating tables to store your policies, see the following topics:

-   [Insurance product models](insurance-product-models.md): Define the product models to reflect your available insurance products.
-   [Coverage specification](coverage-specification.md): Define the coverage specifications for your products, such as what coverage is included and any available options.
-   [Setting up an insurance policy for Insurance claims](set-up-an-insurance-policy.md): Create tables to store your personal and commercial policies.

**Related topics**  


[Insurance product models](insurance-product-models.md)

[Coverage specification](coverage-specification.md)

[Setting up an insurance policy for Insurance claims](set-up-an-insurance-policy.md)

[Policy snapshots in Insurance claims](policy-snapshots.md)

