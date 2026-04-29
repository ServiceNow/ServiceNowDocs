---
title: Add forms to UI Builder pages
description: Use the Form component to add one or more forms to UI Builder pages.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add forms to UI Builder pages

Use the Form component to add one or more forms to UI Builder pages.

Add functionality to your UI Builder pages by including forms. You define the fields on the form and their properties, such as making them required. Then, collect data as the form is completed and submitted.

You can add more than one form to a single page. You can also add a form to a page that already contains a component with a nested form. Sample use cases include:

-   Extend record pages by adding an inline tab with a form using its own form controller instance.
-   Add modals with a form on a record page.

For existing pages with forms created in a pre-Xanadu ServiceNow release, you must apply a preset to the original form before adding another form to the page. Applying the preset is a prerequisite to adding multiple forms to a page and enables multiple forms to work as expected on a page. The form controller preset should be applied onto all form controllers.

1.  Open the page containing an existing form.
2.  In the data drawer, expand the **Data resources** list and select the original form controller.

    ![Data drawer with Data resources list expanded and black arrow pointing to form controller.](../image/form-controller.png)

3.  Select the **Preset** field.
4.  Select **Form controller preset**.

    ![Edit form controller pop-up with black arrow pointing to preset field and second black arrow pointing to form controller preset option.](../image/form-controller-preset.png)

5.  Select **Apply**.
6.  Select the **X** to close the **Edit Form Controller** pop-up.

    Exactly one of your form controllers should have the **Is mapped to app Shell** property set to true. This property is used to specify the primary form on the page. The primary form is responsible for handling global events. You shouldn't set the property to true for more than one form controller or have zero form controllers with the property set to true.

7.  Open the page containing one or more forms.
8.  In the content tree, select a form.

    ![Content tree with black arrow pointing to a form component.](../image/form-controller-app-shell1.png)

9.  In the configuration panel, on the **Configure** tab, select **Form Controller**.

    ![Form configuration panel with configure tab displayed and black arrow pointing to form controller link.](../image/form-controller-app-shell2.png)

10. On the **Edit Form Controller** pop-up, scroll down in the **Form Controller** list to find the **Is mapped to App Shell** option.

    ![Edit form controller pop-up window with black arrow pointing to is mapped to app shell option.](../image/form-controller-app-shell3.png)

11. Select or clear the option for each form component on the page to confirm that exactly one form controller is mapped to the app shell.

## Advanced form event handling

Experienced developers with knowledge of conflict event handling may find the following details useful.

If isMapped to app shell is set to true, the form handles these events automatically:

-   **Screen Status Changed**
    -   Description: Action to indicate that a form is dirty.
    -   Output: `CTRL_RECORD#SCREEN_STATUS_CHANGED`
-   **Update Configuration Menu Requested**
    -   Description: Action to set record configuration menu items on the avatar menu.
    -   Output: `CTRL_RECORD#UPDATE_CONFIGURATION_MENU_REQUEST`
-   **Phone Requested**
    -   Description: Action to make a call when the CTI plugin is enabled.
    -   Output: `CTRL_RECORD#PHONE_REQUESTED`
-   **Form Loading State Changed**
    -   Description: Action to show a loading spinning when that form is loading data.
    -   Output: `CTRL_RECORD#FORM_LOADING_STATE_CHANGED`

For detailed information about the Form component and its properties, see [Form Overview](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/form%20record%20page/overview) on the ServiceNow Developer Site.

**Parent Topic:**[Customize UI Builder pages using components](work-components.md)

