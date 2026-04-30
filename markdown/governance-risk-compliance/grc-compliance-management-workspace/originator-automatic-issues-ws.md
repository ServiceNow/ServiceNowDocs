---
title: Linking automatically generated issues to a control in many-to-many relationship
description: You can link an automatically generated issue that belongs to a different control as a related issue to a control. The Originator flag helps you to differentiate those control issues that were automatically generated from the controls that were manually created.
locale: en-US
release: zurich
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage controls, Use, GRC Compliance Workspace, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Linking automatically generated issues to a control in many-to-many relationship

You can link an automatically generated issue that belongs to a different control as a related issue to a control. The **Originator** flag helps you to differentiate those control issues that were automatically generated from the controls that were manually created.

## Manually created and automatically generated issues

**Note:** You can identify the origin of an issue whether it was automatically generated or manually created after you link the issue from one control to another only in a control form.

You can create an issue manually for a control when you click the **New** button in the Issues related list of a Control form. For manually created issues, see [Manually create GRC issues](../task/manually-create-issues-ws.md).

However, issues are also automatically generated when there are:

-   **Control test failure**

    If there’s a control test which is linked to a control and when one of the test is marked ineffective and closed, then the control becomes non-compliant. As a result, an issue is automatically generated. Control tests can be design test or operational test which can be marked ineffective and the tests can be common across all controls.

-   **Control attestation failure**

    When the user who is an attestation respondent of a control rejects the control, then the status of the control becomes non-compliant and an issue is automatically generated.

-   **Control indicator failure**

    Similarly, when a control indicator fails, the control becomes non-compliant and an issue is automatically generated.


The source of the issue generation for one or more of the three failures can be tracked with the tags in the **Issue source** field of the Issue details. If there is a control test failure, the **Issue source** field is updated with a tag, **Control Test Failure**. If the issue was created manually, then the Issue source tag is **Ad-Hoc**.

When a control's status moves to non-complaint, all the reasons for non-compliancy are pulled from the **Issue source** field and displayed as **Reasons for non-compliance** in the Status widget of the control's Overview page.

![List of reasons for a control's non-compliance.](../image/ReasonsforNonComp.png "Reasons for non-compliance")

## Handling more than one automatically generated issue while linking to a control

You can add an automatically generated issue that belongs to another control, to a control in an m2m relationship using the **Add** button. However, adding an automatically generated issue from another control to a control with an existing automatically generated issue conflicts the source of the issue generation. To track the source of issue generation, a back-end flag, **Originator**, is used. It is a true or false flag and is false, by default. Originator is flagged true or false, if:

-   An automated issue of another control is associated to the current control, then the **Originator** is false.
-   It is a manual issue of the current control, then the **Originator** is false.
-   It is an automated issue of current control then the **Originator** is true.

1.  When there is an issue that exists with Originator as true, and if a control failure happens, the **Issue source** field of the issue is updated with the source of the issue. For example, there’s an issue with originator as true already present and the issue source is Control test failure. If another control failure happens, such as control attestation failure, then the Issue source is updated with two tags, namely Control test failure and Control attestation failure.
2.  When there is no issue present with Originator as true, and if one of the three control failures happens a new automated issue with originator as true is created. For example, if there's a control attestation failure for a particular control that has no issue linked to the control with the originator as true, then a new automated issue with Issue source as control attestation failure is created and the originator is true.

## Data migration

The logic behind flagging an issue as automatically generated or manually created with the Originator flag is handled automatically when you install the latest plugin. For all automated issues linked to existing controls, the originator flag is true in the m2m records between the control and the issue.

