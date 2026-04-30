---
title: Guided Tour Designer accessibility
description: The Guided Tour Designer has accessibility features so that users can design tours using screen readers and keyboard navigation.The Guided Tour Designer has extended the accessibility features of the ServiceNow platform.
locale: en-US
release: yokohama
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Guided Tours, Adoption services, Configure user experiences]
---

# Guided Tour Designer accessibility

The Guided Tour Designer has accessibility features so that users can design tours using screen readers and keyboard navigation.

For the most part, accessibility functionality is the same for the Guided Tour Designer accessibility is the same as platform accessibility. See [Accessibility features](../../../administer/accessibility-508-compliance/concept/c_SetUpSect508ComplianceFeature.md#).

## Use the Guided Tour Designer with accessibility enabled

The Guided Tour Designer has extended the accessibility features of the ServiceNow platform.

### Before you begin

Role required: guided\_tour\_admin or admin

### Procedure

1.  If accessibility features are not enabled, navigate to **User Administration** &gt; **User Preferences** and enable the preference **glide.ui.accessibility**.

2.  Navigate to **Application** &gt; **Module**.

3.  Navigate to **All** &gt; **Guided Tour Designer** &gt; **Create Tour**.

4.  Press tab to the **Tour Name** field and enter a unique name for the guided tour.

5.  Press tab to the **Application Page Name** field.

6.  Enter part of the name to open a list of pages to scroll through and choose from.

7.  Tab to the **Roles this tour is for** slushbucket and use skip links to select roles.

8.  Click **Create**.

    The selected application page opens in the Guided Tour Designer.

9.  Press tab to the field you want to add a step to.

10. Press tab again and then press Enter to open the **Editing** window for the Guided tour step.

    The editing window has the following features:

    -   An icon for placing the callout. Press Enter to open a list to choose the callout's placement. Only viable callout locations are enabled.
    -   The number of the guided tour step and how many steps have been created. When you create your first step this is step 1/1.
    -   A text box to instruct the user what to do at this step.
    -   A choice list to select the trigger. under **Choose action** field. Only triggers that you can use for the selected element appear in the list.
    -   **Cancel** and **Save** buttons.
11. Continue adding steps until you have completed the tour.

    The tour is saved as you save each step.


### What to do next

Tab to the panel on the right side to edit the name of the tour, copy the tour's URL, and rearrange the tour's steps.

