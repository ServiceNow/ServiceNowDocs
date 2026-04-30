---
title: Configure Eligibility Rules Engine Policies in Grants Management
description: Use the Grants Management Eligibility Rules Engine, powered by Policy as Code Engine \(PaCE\), to manage the life cycle of a policy and create, update, review, and execute policies.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure PaCE Eligibility Framework Engine, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Eligibility Rules Engine Policies in Grants Management

Use the Grants Management Eligibility Rules Engine, powered by Policy as Code Engine \(PaCE\), to manage the life cycle of a policy and create, update, review, and execute policies.

Agencies administering grants management programs must ensure that applicants meet certain eligibility conditions before receiving a grant. With the Grants Management Eligibility Framework, agencies can apply a low code approach to eligibility rule creation and management. This enables agencies to manage a variety of rules, from simple to complex, across multiple programs and with ease.

Define and manage your eligibility rules engine policies in a single management console, the Policy Management Home in CSM Configurable Workspace. In the Policy Home of the CSM Configurable Workspace, you can create, remove, and update the policies used for determining eligibility for an application routed through the Grants Management workspace.

![Admin view of Policy Home on CSM Configurable Workspace](../image/psds_gmp_policy_home.png)

PaCE is a scalable workspace that allows you to set up the foundational elements of the Public Sector Eligibility Framework, use data collectors to create complex policies, save policies as a template to make future policy creation easier, and use config parameters to create reusable policies that can be applied across multiple grant programs.

Here, you can:

-   Create policies.
-   Review existing policies.
-   Assess and implement changes to each policy.
-   Determine if a policy should be used as the template for another policy.
-   Understand why a policy may not be working as expected.

You can create any number of policies, which can be updated as required.

-   **[Create a case API Variable for a PaCE policy in Grants Management ​](../concept/psds-config-gmp-api-variable.md)**  
Create a case API variable to transfer the information collected from the case to the PaCE eligibility rules engine. This will be used when creating a policy and referencing fields on the case.
-   **[Create a case data collector for a PaCE policy in Grants Management](../concept/psds-config-gmp-data-collector.md)**  
Create a data collector within PaCE to use a set of data within a policy.
-   **[Create an eligibility policy in Grants Management using PaCE](psds-config-gmp-create-eligibility-policy.md)**  
Create an eligibility policy using Grants Management Eligibility Rules Engine​ to model eligibility rules that can be used to evaluate grants cases.
-   **[Map an PaCE eligibility policy to a grant model using Grants Management Eligibility Framework](psds-config-gmp-map-eligibility-policy.md)**  
For a eligibility policy to be invoked correctly, it must be mapped to an existing grant model. Map a published eligibility policy to one or more of the grant types that your agency offers.

**Parent Topic:**[Configure PaCE Eligibility Framework Engine for use with Grants Management](../concept/psds-config-gmp-pace.md)

**Previous topic:**[Configure pre-eligibility questions in Grants Management](../concept/psds-config-gmp-config-pre-eligibility.md)

**Next topic:**[Create a case API Variable for a PaCE policy in Grants Management ​](../concept/psds-config-gmp-api-variable.md)

