---
title: Risk Management Framework \(RMF\) step 1 - Categorize the authorization package
description: In the Categorize step, you define the criticality or sensitivity of your information system according to potential worst-case scenarios. This involves selecting NIST information types for the package and using the information types to define the impact levels for the package.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Risk Management Framework \(RMF\) step 1 - Categorize the authorization package

In the Categorize step, you define the criticality or sensitivity of your information system according to potential worst-case scenarios. This involves selecting NIST information types for the package and using the information types to define the impact levels for the package.

## Before you begin

Role required to use **Categorize**: sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer

Role required to write to an authorization package: sn\_irm\_cont\_auth.admin, sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.info\_system\_sec\_officer

Role required to select information types: sn\_irm\_cont\_auth.admin, sn\_irm\_cont\_auth.system\_owner

Role required to write to overridden fields on the Package form: sn\_irm\_cont\_auth.system\_owner

## About this task

When you clicked **Categorize** on the Authorization Package form, an **Impact** field, an **Impact** tab, and an **Information Types** related list appeared on the form.

## Procedure

1.  In the **Information Types** tab, select **Edit**.

    **Note:** As you select the information types, guidance about the selected information type appears, including name, categories, and the Confidentiality, Integrity, and Availability \(CIA\) ratings for the information type.

    ![Information Types selection form](../image/slush.png)

2.  Multi-select the information types you want to select for this authorization package and move them to the Information Type List box.

3.  When you have completed your selections, select **Save**.

    The Information Types related list now contains the guidance information for the information types you selected.

    ![Information Types list](../image/info-type-list.png)

4.  Select the **Impact** tab and review the recommended impacts for the information types you selected.

    **Note:** The impacts displayed in the **Recommended** fields reflect the worst-case scenario of the information types you selected. For example, if you selected an information type with High CIA levels, the **Recommended** fields under the **Impact** tab would all show **High** levels of risk. The CIA levels are used to calculate the overall impact of the information types you selected, which is now displayed in the **Impact** field.

5.  You can override any of the impact levels by modifying the **Overridden** fields and providing a justification.

    As you provide overrides, the **Impact** field is updated accordingly based on the update CIA levels.

    ![Impact override fields](../image/impact-overrides.png)

    **Important:** It is vital that the **Impact** field accurately reflects the impact of the data you are authorizing. All processes downstream from this point relies on that impact level. According to NIST guidelines, the number of controls you must implement depends on the Impact, as follows:

    -   High risk = 343 controls
    -   Moderate risk = 262 controls
    -   Low risk = 125 controls
6.  After you have defined the impact, select **Request Approval**.

    ![Authorization Package categorize to request for approval.](../image/cam-auth-packages-request-approval.png)

    An approval request is sent to the Authorizing Official, who will access My Approvals from the navigation pane and review the information in the package. When approval is received, the package transitions to the **Select** state.


