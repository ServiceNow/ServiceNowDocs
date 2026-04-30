---
title: Add key stakeholders and send privacy assessments
description: Add key stakeholders to a processing activity to identify the key members who are responsible for processing the personal data within the processing activity. You can then send the respective privacy assessments to the stakeholders based on their responsibilities. For example, an entity owner is a key stakeholder for a processing activity.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Add key stakeholders and send privacy assessments

Add key stakeholders to a processing activity to identify the key members who are responsible for processing the personal data within the processing activity. You can then send the respective privacy assessments to the stakeholders based on their responsibilities. For example, an entity owner is a key stakeholder for a processing activity.

## Before you begin

Role required: sn\_privacy.analyst

## About this task

A processing activity can have multiple key stakeholders. While you can add or delete as many key stakeholders as you want, by default, the entity owner is one of the key stakeholders. All the stakeholders can respond to privacy assessments and some stakeholders can also edit the processing activity based on their privileges. Only users with the sn\_privacy.assessment\_responder and sn\_privacy.business\_user can be added as stakeholders. You can add key stakeholders only when the processing activity is either in the **Discover** or **Review** states.

## Procedure

1.  Navigate to **All** &gt; **Privacy Management** &gt; **Privacy Workspace** &gt; **Processing activities** &gt; **All processing activities**.

2.  Open the processing activity to which you want to add key stakeholders.

3.  Click the Key stakeholders related list.

4.  Click **Add**.

    1.  Select the stakeholders to add.

    2.  Click **Add**.

        The key stakeholders are added.

5.  To modify the privileges and responsibilities of a stakeholder, select the name of the stakeholder.

6.  In the **Responsibility** field, provide the responsibilities of the stakeholder.

7.  In the **Processing activity privileges** field, select one of the following options.

<table id="choicetable_qyt_gy1_2sb"><thead><tr><th align="left" id="d83323e153">

Option

</th><th align="left" id="d83323e156">

Result

</th></tr></thead><tbody><tr><td id="d83323e162">

**Respond to privacy assessments**

</td><td>

To enable the stakeholder only to respond to the privacy assessment.**Note:** When you choose this option, the role of the stakeholder changes to sn\_privacy.assessment\_responder

</td></tr><tr><td id="d83323e174">

**Edit processing activity and respond to privacy assessments**

</td><td>

To enable the stakeholder to edit and then respond to the privacy assessment.**Note:** When you choose this option, the role of the stakeholder changes to sn\_privacy.business\_user

</td></tr></tbody>
</table>8.  Click **Save**.

9.  Return to the processing activity using the breadcrumb navigation.

10. To send the privacy assessments to a stakeholder, click **Send privacy assessment**

    1.  From the **Classification** field, select the type of assessment.

    2.  From the **Assessment template** field, select the template you want to use.

    3.  From the **User** field, select the user you want to send the assessment to.

    4.  Click **Send**.


**Parent Topic:**[Using Privacy Management](../concept/using-privacy-mgmt.md)

