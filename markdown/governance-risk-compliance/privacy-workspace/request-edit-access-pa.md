---
title: Access a processing activity from the Employee Center
description: Request edit access to a processing activity directly from the Employee Center to update the details your team is responsible for.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/request-edit-access-pa.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 2
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Access a processing activity from the Employee Center

Request edit access to a processing activity directly from the Employee Center to update the details your team is responsible for.

## Before you begin

Role required: sn\_privacy.business\_user

## About this task

Privacy analysts can add any user as a key stakeholder to a processing activity, even those without privacy roles. To enable users without privacy roles to view and edit a processing activity, they must be granted the sn\_privacy.business\_user role, and then have their processing activity privilege modified by a privacy analyst. To understand processing activity privileges, see [Add key stakeholders to a processing activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/add-stakeholders-to-a-pa.md).

All added stakeholders with the appropriate business user role can access the processing activity directly from the Employee Center by navigating to **GRC tasks** &gt; **Tasks** &gt; **My items** &gt; **Processing activities**. After they review the processing activity and find that it needs updating, they can request edit access. This enables them to edit the related lists of the processing activity they are assigned to.

**Note:** Edit access can be requested for processing activities in the **Discover** state.

## Procedure

1.  Open Employee Center.

2.  Navigate to **GRC tasks** &gt; **Tasks** &gt; **My items** &gt; **Processing activities**.

    This opens a list of processing activities where you're added as a key stakeholder.

3.  Open the processing activity you want to edit.

4.  Select **Request edit access**.

    A confirmation message appears confirming that an email has been sent to the privacy analyst.


## Result

The privacy analyst who owns the processing activity receives an email and reviews the request. The analyst updates your processing activity privilege to **Edit processing activity and respond to privacy assessments**, and assigns the processing activity to you. For steps to assign a processing activity, see [Assign a processing activity to a key stakeholder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/assign-pa-to-keystakeholders.md).

**Note:** If the processing activity is in the **Review** or **Monitor** state, the analyst must move the processing activity back to the **Discover** state before assigning it to you.

After it's assigned, you receive an email with a link to the processing activity.

## What to do next

Edit the processing activity related lists directly from the Employee Center by navigating to **GRC tasks** &gt; **Tasks** &gt; **My pending tasks** &gt; **Processing activities**. Select **Assign back to privacy team** when done to request a review of the updated processing activity.

**Note:** Your edit access is removed when you assign a processing activity back to the privacy team.

**Parent Topic:**[Using Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/using-privacy-mgmt.md)

**Related topics**  


[Respond to a privacy smart assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/respond-to-a-privacy-smart-assessment.md)

[Respond to a privacy screening assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/respond-to-privacy-assmnt.md)

