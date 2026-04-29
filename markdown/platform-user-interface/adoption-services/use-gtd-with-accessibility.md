---
title: Create Guided Tours with accessibility enabled
description: The Guided Tour Designer has accessibility features so that users can design tours using screen readers and keyboard navigation.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Create Guided Tours with accessibility enabled

The Guided Tour Designer has accessibility features so that users can design tours using screen readers and keyboard navigation.

## Before you begin

Role required: guided\_tour\_admin

## About this task

Overall, the accessibility features of the Guided Tour Designer align with those of the ServiceNow AI Platform®. See the [Accessibility features](../../../administer/accessibility-508-compliance/concept/c_SetUpSect508ComplianceFeature.md#) section for more information.

## Procedure

1.  If accessibility features aren’t enabled, navigate to **User Administration** &gt; **User Preferences** and enable the preference **glide.ui.accessibility**.

2.  Navigate to **Application** &gt; **Module**.

3.  Navigate to **All** &gt; **Guided Tour Designer** &gt; **Create Tour**.

4.  Press tab to the **Tour Name** field and enter a unique name for the guided tour.

5.  Press tab to the **Application Page Name** field.

6.  Enter part of the name to open a list of pages to scroll through and choose from.

7.  Tab to the **Roles this tour is for** slushbucket and use skip links to select roles.

8.  Select **Create**.

    The selected application page opens in the Guided Tour Designer.

9.  Press tab to the field you want to add a step to.

10. Press tab again and then press Enter to open the **Editing** window for the Guided tour step.

    The editing window has the following features:

    -   An icon for placing the callout. Press Enter to open a list to choose the callout's placement. Only viable callout locations are enabled.
    -   The number of the guided tour step and how many steps have been created. When you create your first step this is step 1/1.
    -   A text box to instruct the user what to do at this step.
    -   A choice list to select the trigger. from the **Choose action** list. Only triggers applicable to the selected element appears in the list.
    -   **Cancel** and **Save** buttons.
11. Continue adding steps until you have completed the tour.

    The tour is saved as you save each step.


## What to do next

Tab to the panel on the right side to edit the name of the tour, copy the tour's URL, and rearrange the tour's steps.

**Parent Topic:**[Configuring Guided Tours](configure-guided-tours.md)

