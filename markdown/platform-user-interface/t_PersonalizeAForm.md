---
title: Personalize a form
description: When the form personalization feature is activated, users can personalize fields to appear on a specific form view according to individual preferences. Form personalization is available in Core UI.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Personalize a form

When the form personalization feature is activated, users can personalize fields to appear on a specific form view according to individual preferences. Form personalization is available in Core UI.

## Before you begin

Role required: itil, personalize\_form, or admin

## About this task

Personal form customizations do not affect what other users see on their forms.

In contrast to configuring a form, personalizing a form does not enable users to perform the following actions:

-   Change the order of fields on the form.
-   Add fields that are not configured to appear on the form.
-   Hide mandatory fields.

**Note:** Personalizing a form in this way modifies the form for you only. To make changes to a form that are visible to all users, you must [configure the form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  Open any record.

2.  In the form header, click the personalize form icon.

    The Personalize Form menu appears and hide field icons appear on the form.

    ![Personalize the form](../image/PersonalizeForm.png "Personalize the form")

    A cleared gray check box indicates fields that you previously hid.

    **Note:** Only the fields that the form is configured to display are available in the Personalize Form menu. To add fields to the form, you must configure the form layout.

3.  Clear a check box or click the hide field icon \(![Hide field icon](../image/HideFieldIcon.png)\) by a field.

    Some check boxes are gray and selected. These check boxes indicate fields that cannot be hidden because they are required or are already hidden by UI policies or client scripts.

4.  Click outside the Personalize Form menu to save your changes.

    If you navigate away from the form, the next time you personalize the form you must reset your customizations to show fields that you have hidden.

5.  To restore the default form view, personalize the form and click **Reset**.


**Parent Topic:**[Forms in the classic environment](../concept/c_UsingForms.md)

**Related topics**  


[Administering form personalization](https://www.servicenow.com/docs/access?context=c_FormPersonalizationAdmin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

