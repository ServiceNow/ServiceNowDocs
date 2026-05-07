---
title: View business impact analysis details
description: Use the Details tab to view the general information of the business impact analysis. You can also adjust the recovery time objective and recovery point objective results of the primary element as per your requirement.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Assess impact categories and dependencies of process, Structured workflows for BIA, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# View business impact analysis details

Use the **Details** tab to view the general information of the business impact analysis. You can also adjust the recovery time objective and recovery point objective results of the primary element as per your requirement.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click the link to the record in the **Name** column in the **In Draft** state.

4.  To view the details of the business impact analysis, click the **Details** tab.

    -   **General Information**

        View the general details of an assessment for the Business Impact Analysis such as the name of the BIA, its description, and the business unit and department that it pertains to. You can also view the template that you have used to create the BIA.

    -   **Results**

        You can track the results at the asset level. Hence, the primary scope is to recover the primary element or the asset. Defining recovery requirements depends on the type of disaster and the time by which each asset must be recovered.

        -   **Recovery tier**: The level of criticality at which the primary element is in terms of its recovery.
        -   **Recovery time objective** \(RTO\): The maximum time by which the business should recover the primary element or asset after the business disruption.
        -   **Adjusted RTO**: If you want to adjust the calculated RTO, then edit this field to add your value.
        -   **Reason for adjusted RTO**: Enter the reason for adjusting the RTO value.
        -   **Recovery point objective** \(RPO\): Point in time at which the primary element must be restored following a disaster. It also indicates the maximum amount of data loss that a business can sustain during a disruptive event.
        -   **Adjusted RPO**: Edit this field to enter your RPO for the primary element.

            **Note:** **Recovery point objective** and **Adjusted RPO** fields appear only if the primary element requires data backup and is flagged as **Yes** in the [Element Definition form](configure-element-definitions.md).

        -   **Reason for adjusted RPO**: This field appears when you enter a value in the **Adjusted RPO** field. Enter the reason for adjusting the RPO value.
        -   **Confidentiality**, **Integrity**, and **Availability**: If the primary element includes critical data, then add Confidentiality, Integrity, and Availability \(CIA\) details. CIA details are basic security goals that the BIA must be compliant with. Non-compliance to these standards may lead not only to huge business and productivity loss but also credibility loss.

            **Note:** The **Confidentiality**, **Integrity**, and **Availability** fields appear only if you have already set the **Include CIA** field as **Yes** in the [Configure a business impact analysis template](configure-bia-template.md) that you have used.

            If you have not adjusted the RTO and RPO values, you can still view the system-calculated RTO and RPO values in their respective fields.

    -   **Activity**

        Additional comments about the BIA.

5.  Click **Save**.

6.  Click the **Generate PDF** button to generate the BIA in a PDF format.

    A message appears that the PDF has been generated.

    ![Success message for PDF generation](../image/PDFDownload.png "PDF download")

    Click the link in the message to download the PDF.

    -   If you have view-only access to the BIA, the option to generate a PDF helps you to download the document to your local hard drive.
    -   You can download the BIA before its **Approval** state.
    -   By default, the PDF is generated and attached after the BIA is approved.
7.  To move a BIA from **Approved** to **Draft** state, click the **Edit** button.

8.  To create a copy of the BIA, click **Copy** button.

    If you have the permission to read and create a BIA, then you can also copy the BIA.

    1.  Enter the name of the new BIA in the Copy impact analysis pop-up.

        The copy action creates an exact replica of the BIA with the name that you enter in the Copy impact analysis pop-up. It also copies all its dependencies and dependency groups on to the new BIA.

    2.  Click **Confirm**.

        -   The new BIA that is copied from the original BIA has all the RTO, RPO impact, dependency assessment structural details similar to the original BIA.
        -   However, the impact category details for each of these assessments are editable for you to assess the dependency details exclusively for the copied BIA.
        -   If the impact categories of the RTO and RPO impact assessments in the original BIA are in the **Complete** state, then the impact categories in the copied BIA are in the **Complete** state.
        -   Therefore, you must assess and enter the disruption duration, response, and required recovery timeframe relevant to the copied BIA.
        -   You can assess the details in the **Results** section. The RTO and RPO values are recalculated after you complete the assessments.
        -   Activities and Work notes are not copied to the new BIA. Enter this information relevant to the new BIA.
        -   Any attachments attached to the original BIA in any format are copied to the new BIA. However, the PDF generated for the original BIA using the **Generate PDF** button will not be copied over to the new BIA as the assessment data pertain to the original BIA. Since you have the flexibility to modify the assessment details in the copied BIA and generate a PDF, copying the PDF generated for the original BIA has no relevance.
        **Note:** You can delete a BIA and its related tables in the **Draft** state. The BCM planner and program manager can delete a BIA that is in the **In Review** and **Returned** states whereas, a BCM admin can delete a BIA irrespective of its state.


