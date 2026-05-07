---
title: Sales promotion
description: OEMs create sales promotions and discounts targeted to specific criteria or customers. Channel partners extend these promotions to end customers during sales transactions, and the OEM reimburses dealers for the discounts offered.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [MCO core, Explore, Manufacturing Commercial Operations]
---

# Sales promotion

OEMs create sales promotions and discounts targeted to specific criteria or customers. Channel partners extend these promotions to end customers during sales transactions, and the OEM reimburses dealers for the discounts offered.

This feature enables the seamless collaboration between OEMs and their dealers to manage sales promotions and claims. The sales promotion framework enables the OEMs to publish and manage the promotional campaigns efficiently. The dealer portal enables the dealers to submit claims for reimbursement post product sales transactions.​ There are three parts to the sales promotion​.

-   Creation of sales promotion by the OEM.
-   Creation of claim against the promotion by the dealer.
-   Review and reimbursement for the claim by the OEM.

![Sales promotion workflow](../image/salespromotion-claim-wf.png "Sales promotion workflow")

1.  Create sales promotion: OEM creates the sales promotion campaign.
2.  Associate products: OEM adds the products applicable for the sales promotion campaign.
3.  Set up incentive: Set up the incentive for the dealers.
4.  Add dealers: Add the dealers who are eligible for the sales promotion campaign.
5.  Set up questionnaires: Configure the promotion questionnaires.
6.  Set up checklist: Configure the checklist template.
7.  Publish: OEM publishes the sales promotion campaign for the applicable dealers.
8.  Create sales promotion claim: The dealer agent creates the promotion claim for the applicable customers.
9.  Search serial number: Add the product, which is applicable for sales promotion campaign.
10. Select applicable promotion: Select the applicable promotion from the list of promotions.
11. Fill in the claimed amount: Update the claimed amount for the selected promotion.
12. Fill in the questionnaires: Update the promotion questionnaires.
13. Add attachments: Add the attachments, if necessary.
14. Submit claim case: The dealer agent submits the claim to the OEM.
15. Sales promotion claim case: A claims agent can view the list of sales promotion submitted by the dealer.
16. Review sales promotion case line: A claims agent reviews the claims.
17. Verify checklist: Verifies the checklist.
18. Approve: Approves the claims if it matches all the required criteria.
19. Expense line: Expense line is generated for the approved claims.
20. Process payment: The payment is processed.
21. Close sales promotion claim: The claim is closed.
22. Reject claim: Rejects the claims if it doesn’t match the required criteria.

## Working with sales promotion

Use the following to configure, use, and manage the sales promotions in MCO.

Review the entities and relationships within the [Sales promotion campaign data model](../reference/sales-promotion-campaign-claims.md) application, including tables added or modified by the sales promotion plugin.

1.  Configure the sales promotion: Complete the following tasks to set up sales promotion in your environment.
    1.  Install Sales promotion claim management \[sn\_sls\_prm\_clm\_mgt\]: [Installing applications, plugins, and products](https://www.servicenow.com/docs/access?context=installing-apps-app-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    2.  Set up product models and parts: [Configuring product models](mco-product-models.md)
    3.  Set up assets and install base items: [Configuring assets](mco-assets.md) and [Create an install base item](mco-create-install-base-item.md)
    4.  Set up dealers: [Set up dealer](set-up-dealer.md)
    5.  Assign recall roles: [Assign roles](assign-mco-roles.md)
    6.  [Set up sales promotion](mco-set-up-sls-prom.md)
2.  Work with sales promotion \(OEM\): Use the Agents \(CSM/FSM\) workspace to create and manage sales promotion campaigns and review claims.
    -   [Sales promotion management](mco-sls-pro-mgmt.md)
    -   [Sales promotion claim management](mco-sls-pro-clm-mgmt.md)
3.  Work with sales promotion \(Dealer\): Use the Dealer portal to submit and track sales promotion claims.
    -   [Submit a sales promotion claim](../task/mco-sales-promotion-single-claim.md)
    -   [Upload a bulk sales promotion claim](../task/mco-sales-promotion-bulk-upload.md)

