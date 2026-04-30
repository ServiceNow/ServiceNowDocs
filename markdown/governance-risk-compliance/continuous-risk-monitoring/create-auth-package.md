---
title: Create an authorization package
description: After you have defined the authorization boundaries for the assets or systems to send through the Authorization to Operate process, you must create an authorization package for that purpose. The package is processed through the seven steps mandated by the RMF.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [RMF step 0 - Prepare the authorization package, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Create an authorization package

After you have defined the authorization boundaries for the assets or systems to send through the Authorization to Operate process, you must create an authorization package for that purpose. The package is processed through the seven steps mandated by the RMF.

## Before you begin

Role required: sn\_irm\_cont\_auth.system\_owner or sn\_irm\_cont\_auth.admin

**Note:** The roles are required for accessing the authorization package only after it has transitioned beyond the Prepare state.

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization &amp; Monitoring** &gt; **All Authorization Packages**.

    ![Authorization packages](../image/cam-auth-packages.png)

2.  Select **New** and then fill in the form.

    The settings are described in [Fields on the Authorization Package form](../reference/cam-form-authorization-package.md).

    ![Authorization package - new](../image/cam-auth-packages-new.png)

3.  Select the **Roles and Responsibilities** tab and specify the responsibilities of various stakeholders during the review and approval process.

    The settings are described in [Roles and Responsibilities](../reference/cam-form-authorization-package.md#section_xml_sf4_qfc).

4.  Select the **PTA/PIA** tab and perform the Privacy Threshold Analysis by answering the questions.

    The PTA identifies whether various types of the Personal Identifiable Information \(PII\) exist in the systems being authorized.

    ![Privacy Threshold Analysis/Privacy Impact Assessment](../image/pta-pia.png)

5.  If you answered **No** to all of the questions, you are not required to take a Privacy Impact Analysis and can select **Submit**.

6.  If you answered **Yes** to any of the questions, you must take a Privacy Impact Analysis.

    1.  In the Assessment respondents field, select the lock icon and select the users you want to take the assessment.

    2.  When you have selected the respondents, select the lock icon again.

    3.  Select **Submit**.

        The assessment request notification is sent to the selected respondents.

    4.  When the PIA has been completed, the assessment responses appear in a related list in the Authorization Package form.

7.  Select the **Notes and Comments** tab to add any customer-facing notes to the package.

8.  Select **Proceed to Next Step** to transition the package to the next step.

    The authorization package is transitioned to categorize step.![Authorization Package proceed to next step.](../image/cam-auth-packages-next-step.png)


**Parent Topic:**[Risk Management Framework \(RMF\) step 0 - Prepare the authorization package](../concept/prepare-auth-pkg.md)

