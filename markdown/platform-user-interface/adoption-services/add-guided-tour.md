---
title: Create a guided tour
description: After you outline the guided tour, use the Guided Tour Designer \(GTD\) to enter the steps using callouts and triggers.
locale: en-US
release: xanadu
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Using Guided Tours, Guided tours, Adoption services, Configure user experiences]
---

# Create a guided tour

After you outline the guided tour, use the Guided Tour Designer \(GTD\) to enter the steps using callouts and triggers.

## Before you begin

Role required: guided\_tour\_admin or admin

## About this task

This task is an example that illustrates how to create a guided tour for assigning a vacation delegate.

## Procedure

1.  Navigate to **All** &gt; **Guided Tour Designer** &gt; **Create Tour**.

2.  Complete the fields on the form.

<table id="table_ujy_ssw_ty"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the tour that describes what the user accomplishes by completing it. For example, in this case, `Set a vacation delegate`.

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

Select the page the tour starts on. -   If your Tour Type is Standard UI, your choices include pages that show lists and forms.
-   If your Tour Type is Service Portal, your choices include Service Portal pages.

**Note:** In the base system, you can only launch tours from pages that use the SP Header Menu. Manually launched tours do not display on pages with custom header menus.

-   If your Tour Type is Custom UI, your choices include pages that show Custom UI pages.
-   If your Tour Type is Workspaces, your choices include pages that show Workspaces pages. You can select the page in two ways:
    -   Paste URL: You can copy the URL of the workspace page and paste it. If the URL is not a valid experience, the **Create Tour** button is not enabled.
    -   Manual Selection: You can select the page from the dropdown by typing the name of the page.

**Note:** If the selected page contains parameters, you must mention the values of the parameters. You can configure the the page parameters as dynamic if you want the tour to apply to the same page without exact parameters.

 You can begin typing the UI page name to show a list of matching pages, and then select it from the list.

 **Note:** In some cases, navigating to standard forms and lists while creating custom tours might not work as expected. You can choose a following workaround to create the custom UI tour in such cases.

1.  Create standard UI type tour on any page, ideally home page.
2.  Go to system property - `com.snc.guided_tours.homepages` and add the name of the custom page in the **Value** field of this page. You can enter multiple values separated by commas.
3.  Update the context of the tour from form view to your custom page.


</td></tr><tr><td>

Roles

</td><td>

-   If the tour can be accessed by all the roles, then select **All**.
-   If the tour can be accessed by specific roles, then select **Specific**.
 Select the roles that can access this guided tour and move them to the **Roles that can view the tour** list from **Available Roles** list.

 **Note:** When you add at least one role to a tour, it limits the audience to only those users who have that role.

</td></tr></tbody>
</table>3.  Click **Create**.

    The Guided Tour Designer opens in draft status in a new tab or window. In this example, no records are displayed in the list as new delegates are created.

    ![Shows Delegate role page with the list of delegates. In this example, no records are displayed in the list as new delegates are not created in the instance.](../image/create-guided-tour-madrid.png)

4.  Click **Create Introduction**.

    1.  Enter an introductory title for your guided tour, such as `Cover your approvals during your vacation`.

    2.  Type a message to your end users introducing the goal of the demo, such as `Join this tour to learn how to create a vacation delegate.`

    You can edit and delete introductions, conclusions, and callouts at any time while your tour is in draft status. You can also insert HTML markup into your Conclusions, Introductions, and callouts.

    All standard HTML tags compatible with your browser are supported.

5.  Complete the following steps to add a tour step with a callout and trigger.

    1.  Drag a callout shape from the upper right corner of the screen and drop it on top of the UI element.

        The element is highlighted when the callout is positioned correctly. When you release the callout, it locks into the position.

        ![Callout positioned correctly](../image/guided-tour-drop-callout.png)

    2.  Once the callout is placed at the right position, Create Step page appears.![Create Step Page](../image/gtd-createstep.png)

    3.  Enter the instructions in the **Text** box on the panel at the right.

    4.  Change the direction of the callout by selecting the appropriate option under **Placement**.

        Only placement options that you can use for the selected element are enabled in the options.

    5.  [Select the trigger](../reference/guided-tour-triggers.md) under **Choose action** field. Only triggers that you can use for the selected element appear in the list.

        ![Callout trigger](../image/guided-tour-delegate-callout-london.png)

    6.  To apply text formatting, such as bold or italic, add html tags around the text to format.

        For example, enter `Click <b>New</b> to set up a delegate...`. You can add other HTML tags, including tags for images.

    7.  Select the **Skippable** check box if a user can skip the step and proceed to the next if an element or field is unavailable at runtime.

    8.  Click **Save**.

        Your first step label appears.

        ![Tour first step callout label](../image/guided-tour-step1-label-london.png)

        When your end users click the label, they see your first step instructions rendered as a message.

        ![Tour first step label is rendered](../image/guided-tour-step1-rendered-london.png)

6.  Continue adding steps until you have completed the tour.

    The tour is saved as you save each step.

7.  Click **Create Conclusion**.

    Enter a message to your end users that concludes the demo, and summarizes what they accomplished. For example, enter `Congratulations! You just created a delegate to take care of things while you're on vacation. Have fun!`.

8.  Click **Save**.

    Your Conclusion message appears after your last tour step, showing the final result of the tour. When users click **Complete**, the tour ends.

    ![Closing step in a guided tour — Madrid UI](../image/gtd-closing-note-london.png)

9.  Click **Preview** at any time to test your steps and make any final revisions to the tour until you are satisfied.

    Note the steps that are not working properly or that need correction. Edit the tour or the steps as described in [Edit a guided tour](edit-guided-tour.md).

10. To share your draft or published tour with internal colleagues for review, you can:

    1.  Click the Copy URL icon ![Show the user the Copy URL icon for guided tours.](../image/gtd-paperclip-icon.png) to copy the tour URL.

    2.  Send the URL to reviewers.

11. Click **Publish** to make your guided tour visible to your end users.

    Each guided tour is allotted with a unique tour ID when it is created. The tours appear in alphabetical order if you set property **\(com.snc.guided\_tours.sort\)** to true. When users access a starting page of the guided tour, they can access the tour from the following.

    -   If the tour type is Standard UI, they can click **Take a Tour** in the Help Center.
    -   If the tour type is Service Portal, they can click **Tours** on the banner of the page.

**Related topics**  


[Exploring Guided Tours](../concept/exploring-guided-tours.md)

