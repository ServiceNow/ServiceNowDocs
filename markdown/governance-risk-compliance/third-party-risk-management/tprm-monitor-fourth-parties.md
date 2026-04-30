---
title: Monitoring your fourth-nth parties
description: You can identify and manage the third-party risks that depend on the services of the fourth-nth parties by using the Third-party Risk Management application. By monitoring your fourth-nth parties, you can help to ensure that they adhere to the same security and compliance standards as the primary third party.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Monitor third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Monitoring your fourth-nth parties

You can identify and manage the third-party risks that depend on the services of the fourth-nth parties by using the Third-party Risk Management application. By monitoring your fourth-nth parties, you can help to ensure that they adhere to the same security and compliance standards as the primary third party.

## Fourth-nth parties

Fourth-nth parties can include various entities, such as sub-suppliers, service providers, consultants, or any other organization that the third party relies on to deliver its products or services. These parties could have access to your sensitive data, systems, or processes, which makes them potential sources of risk.

Let's look at some fourth-nth party risk examples:

-   **Parts**

    A company regularly uses an item from a third party that relies on a hardware part from another organization. In this case, the organization that provides the additional part is a fourth party that can potentially create a downstream risk for the item that is provided by the third party.

-   **Services**

    A company stores its payroll application by using the Automatic Data Processing \(ADP\) service. The ADP service is a third-party service that relies on Amazon Web Services \(AWS\) to store its data. The ADP service depends on AWS to have security measures and processes in place to safeguard their data and maintain its safety. Although AWS is often a third party of primary services, the AWS service is a fourth party to the third party ADP in this case.


You can link two fourth parties to each other. For example, a link can occur when an organization that provides an additional part relies on another fourth party to deliver the hardware part. However, you can't create a loop when you link two fourth parties. The starting point can be either a third or fourth party. For example, let's consider Fourth party A, which has a child Fourth party B. Fourth party B, in turn, has a child Fourth party C. However, Fourth party C can’t have a child that leads back to Fourth party A. This restriction ensures that a circular dependency isn’t formed among the fourth parties.

## Fourth-nth party actions

As part of your risk management program, you can add fourth-nth party information manually or by collecting responses from a third party by using a fourth-party registration questionnaire. You can manually create a fourth-nth party record if you don't have time to send a questionnaire to a third party or only need to create one record. After reviewing and registering, or manually creating these fourth-nth party records, they’re available for monitoring by using Vendor Management Workspace. As your business relationships change, you can keep relevant information current by promoting a fourth-nth party record to a third-party record. This third-party record incorporates all existing information and then designates the existing fourth-nth party as a known fourth party.

Here are the different actions that you can take to manage and monitor fourth-nth parties:

-   **Register the fourth-nth parties**

    If you're a third-party risk \(TPR\) assessor or manager, you can register fourth-nth parties after collecting responses from a third party by using the fourth-party registration questionnaire. You can send the fourth-party registration questionnaire only to the third parties and not engagements. For more information, see [Register a fourth-nth party](../task/tprm-fourth-party-register.md).

-   **View the fourth-nth parties that are associated with a third party**

    You can view all the related fourth-nth parties by navigating to the **Downstream suppliers** tab of the third-party page in Vendor Management Workspace. Viewing all the fourth parties that are linked to a third party can help you make informed decisions about initiating or continuing a relationship with an engagement. For instance, if a fourth party that is associated with a third party is known for higher risks in the automotive industry, it might still be acceptable to pursue an engagement in a different industry. However, if an engagement with the same third party involves the automotive industry, the risk could be considered too high.

    For more information on how to view all the related fourth-nth parties, see [Viewing information on fourth parties](../../grc-workspace-vrm/reference/tprm-ws-tab-tp-downstream-suppliers.md).

-   **View the fourth-parties overview section**

    You can view the known fourth parties, the sub-parties that are associated with the third parties, and the unknown fourth parties by navigating to the Vendor Management Workspace home page. Having this high-level view is helpful in understanding how much information is available for a fourth party and how it relates with the other third parties and engagements. For example, if it’s a known fourth party, you can leverage all the existing due diligence information that was gathered while it was assessed as a third party.

    **Note:** The known fourth parties are organizations that have already been used as third parties in your risk management program. The unknown fourth parties are only categorized as fourth parties that haven’t been used or identified as third parties.

    For more information on viewing the known fourth parties, the sub-parties that are associated with the third parties, and the unknown fourth parties, see [TPRM Home page](../../grc-workspace-vrm/concept/tprm-ws-home-page.md).

-   **Manually create a fourth-nth party record**

    If you’re a TPR assessor or manager, you can manually create a fourth-nth party record.

    For more information on how to create a fourth-nth party record, see [Create a fourth-nth party record](../task/tprm-fourth-party-create.md).

    **Note:** You can add an existing third party as a fourth-nth party to another third party by navigating to the **Downstream suppliers** tab of a third-party page in the Vendor Management Workspace and selecting **Add**. After it’s added the existing third party is now categorized as both a third party and fourth-nth party for the chosen third party and includes all collected information.

-   **Promote a fourth-nth party to a third party**

    If you’re a TPR assessor or manager, you can promote a fourth-nth party record to a third party. After you promote a fourth-nth party to a third party, a third-party record is created and the existing fourth-nth party is identified as a known fourth party.

    For more information on how to promote a fourth-nth party record to a third-party record, see [Promote a fourth-nth party to a third party](../task/tprm-fourth-party-promote.md).


**Related topics**  


[Viewing information on fourth parties](../../grc-workspace-vrm/reference/tprm-ws-tab-tp-downstream-suppliers.md)

[TPRM Home page](../../grc-workspace-vrm/concept/tprm-ws-home-page.md)

