---
title: Request due diligence for a third-party engagement
description: Request due diligence to assess the risk that is associated with doing business with an engagement. By conducting due diligence, you gain access to the most up-to-date, comprehensive, and accurate information before making a decision on entering into a business relationship.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Request due diligence, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Request due diligence for a third-party engagement

Request due diligence to assess the risk that is associated with doing business with an engagement. By conducting due diligence, you gain access to the most up-to-date, comprehensive, and accurate information before making a decision on entering into a business relationship.

## Before you begin

Role required: snc\_internal

## About this task

Because your organization assesses the risk that is associated with doing business with third parties, it performs due diligence for any engagement with a third party. When you request due diligence, you specify the third party's name and the reason for your request. For example, start a new engagement with a third party that you have already engaged or perform due diligence in preparation to renew a contract. You then specify the details that help the Third-party Risk \(TPR\) managers and TPR assessors at your organization proceed with the due diligence processes. If a request is accepted, it initially goes through the IRQ process. After the IRQ process, as part of the Due diligence process, two third-party risk assessments begin. One assessment is for the third party and another assessment is for the engagement. For more information, see [Due diligence workflow](../concept/tprm-workflow-in-workspace.md).

**Note:** This feature is available only if the Third-party Risk Management application has been activated. After you install the Risk concentration map feature, you must install a Google license to enable the feature. To enable the risk concentration map feature, see [Enable the TPRM Risk concentration map](../../grc-vendor-risk-implementation/task/tprm-risk-map-configure.md).

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** to open your Employee Center and then select **Risk &amp; Compliance**.

2.  Select the **Request due diligence for third-party risk** card.

3.  On the request form, specify the purpose of your request.

    -   **Onboard a new engagement**
    -   **Reassess an existing engagement**
    -   **Reassess an existing engagement for contract renewal**
    -   **Offboard an engagement with due diligence**
    -   **Offboard an engagement with no due diligence**

        For more information, see [Offboarding an engagement without conducting due diligence](../concept/tprm-dd-request-offboard-no-dd.md).

    For descriptions of each type of due diligence request, see [Requesting third-party risk due diligence](../../grc-vendor-risk/concept/tprm-requesting-tpr-due-diligence.md).

4.  Select **Add attachments** to include a document with the request.

5.  Specify the third party for the engagement.

    You can request due diligence either for an engagement with a third party that you’re already engaged with or for an engagement with a new third party.

    **Note:** You can reactivate a third party that is in the **Terminated** status. Terminated third parties appear in the list for requests of the **Onboard a new engagement** type. If such a request is accepted and closed, the third party's status is changed to **Active**.

    -   For an engagement with an existing third party or with a department, partner, subsidiary, or fourth party of the third party:
        1.  Select the third party from the list.
        2.  The form expands and the system auto-populates the key information for the third party including the address and contact details.
        3.  In the next step, enter the key information like the address and contact details for the engagement.
    -   For a new third party:
        1.  Select the **Third party is not listed** check box.
        2.  Enter the name of the new third party.
        3.  The form expands. In the next step, you enter the key information like the address and contact details for the third party and for the engagement.
    If you selected an existing third party, much of the information is automatically filled in. For descriptions of these fields, see [Request third-party risk due diligence request form](../reference/tprm-dd-form.md).

6.  Select **Submit**.

    -   The system opens to the **Activity** tab on the My request page. For each due diligence request, the system auto-assigns a unique ID number that starts with the text DDR. Use the ID to track your request. You can post a message to reviewers and add attachments from the page.
    -   The system sends you an email confirmation that your request was submitted. The message includes a link to the request details on the Third-party Risk Management application.
    -   The system sends an email notification to all users in the group that is specified in the **Assignment group**. The message states that the request was received and is in the **New** state. The message also includes a link to the details page for the request.
    **Note:** For new due diligence requests, the **Assignment group** is set to Due diligence request assigners. The TPR manager or owner can specify which group is the **Assignment group** on the **Details** tab for a due diligence request. For more information, see [Due diligence request process management](../reference/tprm-ws-dd-mgt-pg-details-tab.md) and [Add users to groups based on responsibilities](../../grc-vendor-risk-implementation/task/tprm-groups-add-users-to.md).


**Related topics**  


[Offboarding an engagement without conducting due diligence](../concept/tprm-dd-request-offboard-no-dd.md)

