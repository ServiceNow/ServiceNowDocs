---
title: Create Guided Tours
description: After you outline the guided tour, use the Guided Tour Designer \(GTD\) to enter the steps using callouts and triggers.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Create Guided Tours

After you outline the guided tour, use the Guided Tour Designer \(GTD\) to enter the steps using callouts and triggers.

## Before you begin

Role required: guided\_tour\_admin

## About this task

This task illustrates how to create a guided tour.

## Procedure

1.  Navigate to **All** &gt; **Guided Tour Designer** &gt; **Create Tour**.

2.  Enter the following information in the form:

<table id="table_ujy_ssw_ty"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the tour that describes what the user accomplishes by completing the tour.

</td></tr><tr><td>

Tour Type

</td><td>

Select:-   **Standard UI** for tours that start from system platform content, such as a list or a form.
-   **Service Portal** for tours that start from a Service Portal page.

**Note:** When you select **Service Portal**, a **Portal** option appears, where you choose a record from the Service Portals table.

-   **Custom UI** for tours that start from Custom UI page.
-   **Workspaces** for tours that start from a Workspace page.


</td></tr><tr><td>

Starting Page

</td><td>

Select the page that the tour starts on:-   If your tour type is Standard UI, your choices include pages that show lists and forms.
-   If your tour type is [Service Portal](../../service-portal/concept/c_ServicePortal.md), your choices include [Service Portal](../../service-portal/concept/c_ServicePortal.md) pages.

**Note:** In the base system, you can only launch tours from pages that use the SP Header Menu. Manually launched tours do not display on pages with custom header menus.

-   If your tour type is Custom UI, your choices include pages that show Custom UI pages.
-   If your tour type is Workspace, your choices include pages that show Workspaces pages. You can select the page in two ways:
    -   Paste URL: You can copy the URL of the workspace page and paste it. If the URL isn’t a valid experience, the **Create Tour** button isn’t enabled.

**Important:** The maximum length for URLs is 2,500 characters. If a URL exceeds this limit, it is automatically truncated to the first 2,500 characters.

    -   Manual Selection: You can select the page from the drop-down menu by entering the name of the page.

**Note:** If the selected page contains parameters, you must mention the values of the parameters. If you want the tour to apply to the same page without exact parameters, configure the page parameters as dynamic.

You can begin entering the UI page name to show a list of matching pages, and then select it from the list.

**Note:** In some cases, navigating to standard forms and lists while creating custom tours might not work as expected. You can choose the following workaround to create the custom UI tour in such cases:

1.  Create standard UI type tour on any page, ideally home page.
2.  Go to system property - `com.snc.guided_tours.homepages` and add the name of the custom page in the **Value** field of this page. You can enter multiple values separated by commas.
3.  Update the context of the tour from form view to your custom page.


</td></tr><tr><td>

Roles

</td><td>

-   If the tour can be accessed by all the roles, then select **All**.
-   If the tour can be accessed by specific roles, then select **Specific**.

Select the roles that can access the guided tour and move them from the Available Roles list to the Roles that can view the tour list.

 **Note:** When you add at least one role to a tour, it limits the audience to only those users who have that role.

</td></tr></tbody>
</table>3.  Select **Create**.

    The Guided Tour Designer opens in draft status in a new tab or window.

    ![Shows Guided Tour Designer in a new tab.](../image/create-guided-tour-madrid.png)

4.  Select **Create Introduction**.

    1.  Enter an introductory title for your guided tour.

    2.  Write a message to your end users explaining the purpose of the tour.

    3.  Select **Save**.

5.  Follow these steps to add a tour step with a callout and trigger:

    1.  Drag a callout from the upper right corner of the screen and drop it on top of the UI element.

        The element is highlighted when the callout is positioned correctly. When you release the callout, it locks into the position.

        ![Callout positioned correctly](../image/guided-tour-drop-callout.png)

    2.  Enter the instructions in the **Text** box.

        ![Create Step Page](../image/gtd-createstep.png)

        You can change the direction of the callout by selecting the correct option under **Placement**. Only the placement options applicable to the selected element are enabled.

    3.  [Select the trigger](../reference/guided-tour-triggers.md) from the **Choose action** list. Only triggers applicable to the selected element appears in the list.

        ![Callout trigger](../image/guided-tour-delegate-callout-london.png)

    4.  To format text, such as bold or italic, add HTML tags around the text.

        For example, enter `Click <b>New</b> to set up a delegate`. You can add other HTML tags, including tags for images.

    5.  Select the **Skippable** check box if a user can skip the step and proceed to the next if an element or field is unavailable at runtime.

    6.  Select **Save**.

        The first Step label appears.

        ![Tour first step callout label](../image/guided-tour-step1-label-london.png)

        When your end users select the label, they see your first step instructions rendered as a message.

        ![Tour first step label is rendered](../image/guided-tour-step1-rendered-london.png)

6.  Continue adding steps until you have completed the tour.

    The tour is saved as you save each step.

7.  Select **Create Conclusion**.

    1.  Enter a closing message for the demo that summarizes the users' achievements.

    2.  Select **Save**.

    **Note:** You can edit and delete introductions, conclusions, and callouts at any time while your tour is in draft status. You can also insert HTML markup into your conclusions, introductions, and callouts.

    All standard HTML tags compatible with your browser are supported.

8.  Select **Preview** at any time to test your steps and make any final revisions to the tour.

    Note the steps that aren’t working properly or that need correction. Edit the tour or the steps as described in [Edit Guided Tours](edit-guided-tour.md).

9.  To share your draft or published tour with your internal colleagues for review, do the following:

    1.  Select the copy URL icon ![Copy URL icon](../../../reuse/icons/product-icons/link-outline-24.svg) to copy the tour URL.

    2.  Send the URL to reviewers.

10. Select **Publish** to make your guided tour visible to users.


## Result

The guided tour is created and listed in the Help Center. Each guided tour is allotted with a unique tour ID. If you set property **\(com.snc.guided\_tours.sort\)** to **true**, the tours appear in alphabetical order.

**Related topics**  


[Exploring Guided Tours](../concept/exploring-guided-tours.md)

