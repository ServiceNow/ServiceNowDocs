---
title: Mobile Platform release notes
description: The ServiceNow Mobile Platform application enables you to access your ServiceNow instance from anywhere. Mobile Platform was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
---

# Mobile Platform release notes

The ServiceNow® Mobile Platform application enables you to access your ServiceNow instance from anywhere. Mobile Platform was enhanced and updated in the Yokohama release.

## Mobile Platform highlights for the Yokohama release

-   Write and refine text with the Now Assist Context Menu.
-   Use enhanced capabilities within the input form screen.

See [Mobile Platform](https://www.servicenow.com/docs/access?context=mobile-config-navigation&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Now Assist Context Menu](https://www.servicenow.com/docs/access?context=now-assist-context-menu-mobile&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Write and edit text natively from within your mobile app using the Now Assist Context Menu. Refine your selected text by asking Now Assist to shorten it, make it more elaborate, or change the tone, and so on. Now Assist Context Menu is supported for the Task Summarization skill for input form screens.

-   **[Single instance login](https://www.servicenow.com/docs/access?context=mobile-instances-admin-concept&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Customers with a single instance can bypass the instance selection page and navigate users directly to the login screen. This process shortens the login process.

-   **[Display a customized page before user login](https://www.servicenow.com/docs/access?context=branded-landing-page&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Configure your own branded landing page to appear before users log in to their ServiceNow mobile apps. The branded landing page can contain a login button or deep link that redirects users to an area of a ServiceNow mobile app. For example, a municipality can add a button to open a ticket, which navigates the user to complete a record in the Now Mobile® app.

    This feature is available to customers using a single instance, and is supported for both Mobile Publishing apps.

-   **[Define attachment sources available to users](https://www.servicenow.com/docs/access?context=attachment-source-define&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Control the types of attachments used from a phone's gallery, camera, or file system. This capability confirms that images can’t be reused or are AI-generated images. This feature is supported for all attachment locations, including: activity stream, functions with type “attachment”, input form screen with field type “attachment”, Mobile App Bridge, and Cabrillo JS uploads.

-   **[Add annotations to uploaded images](https://www.servicenow.com/docs/access?context=image-annotation-adjust&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Edit and annotate uploaded images within ServiceNow mobile apps. Markup options include adding text, drawing, and highlighting areas. This feature is supported for all attachment locations, including: activity stream, functions with type “attachments”, input form screen with field type “attachment”, Mobile App Bridge, and Cabrillo JS uploads.

-   **[Mobile App Builder live mobile previews](https://www.servicenow.com/docs/access?context=mab-record-example-panel&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    See your mobile content change in real-time with live previews for most mobile components. The mobile interface changes according to what component you have selected, and updates when you add, change, or remove UI-based elements.

-   **[Web to mobile AI card creation](https://www.servicenow.com/docs/access?context=web-mobile-component-conversion&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Use Now Assist to create a new mobile card for use on a record screen created using the Web to Mobile functionality. Now Assist will automatically choose the optimal card template and map the most relevant table fields from the selected web form view.

-   **[Agentic AI in Mobile Virtual Agent](https://www.servicenow.com/docs/access?context=agentic-ai-mobile-va&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Use AI agents in your mobile app to boost live agent productivity. AI agents handle tasks from automated responses to complex problem-solving with human-like intelligence.

-   **[Now Assist in the Virtual Agent mobile client](https://www.servicenow.com/docs/access?context=now-assist-mobile-va&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)Mobile Virtual Agent&gt;**

    Use the following enhancement added to Virtual Agent:

    -   Enhanced chat offers a more robust conversational experience. Check the status of previous and on-going chats with the chat history button and view Now Assist’s responses with streamlined in-line citations. Enhanced chat also allows you to use your custom mobile search configuration to launch the standard search results page from within enhanced chat.
    -   Use Now Assist’s people match function to search for information about a specific employee.
    -   Now Assist can now suggest follow-up actions for your queries using the next best action feature.
    -   Updated UI for choice list pickers and other actions for improved usability.
    -   Added multi-language support.

## UI changes

-   **[Mobile App Builder](https://www.servicenow.com/docs/access?context=mab-concept&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Use the following enhancements added to Mobile App Builder:

    -   Live component preview enables admins to view their mobile app changes in real-time.
    -   Use Mobile App Builder to transform your web forms into native mobile experiences with the guided flow when you create a new mobile record screen.
    -   The right-hand panel is now visible when a record is opened in a preview browser tab.
    -   Component recommendations available for additional record types.
    -   The card selection and preview screens in the Web to Mobile flow have been consolidated to create a more streamlined user experience. This allows for the ability to generate previews using the different card options and jump back and forth between them to review.

## Changed in this release

-   **[Input form screen enhancement and changes](https://www.servicenow.com/docs/access?context=parameter-input-screen&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Use the following enhancements added to the input form screen:

    -   Selecting input values directly within the input form screen, either from a list or from a group of chips. Now users don’t need to navigate to a separate dedicated screen for value selection, when using the inline choice chips layout. You can also define the number of input values to display on an input form screen section.
    -   Ability to add images, plain text, and rich text within specific inputs. These added descriptive elements provide more context to your users and give a clearer idea of what is required for certain inputs. For example, an image can accompany a checklist to ensure that a piece of hardware is wired correctly.
    -   Provide users with the ability to perform actions in relation to the displayed input parameter, while working directly on an input form screen. The available actions are: navigate to another screen, add an attachment from the gallery or camera, and add a comment to a field. Users submit these added actions either when saving their progress or completing the input form screen.
    -   Save input form screen data before it's submitted. Users with access to the same record can see each other's changes either when saving their progress or completing the input form screen.
    -   Interact and switch between other navigation tabs while also working on the input form screen.
    -   Sections are no longer displayed if they don’t contain any input fields.
-   **[Additional number attributes for input form screens](https://www.servicenow.com/docs/access?context=parameter-screen-var-attr&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Use the following number attributes in your input form screens:

    -   Use the **CustomErrorMessage** attribute to specify an error message when a UI rule condition is met.
    -   Use the **SkipValidationWhenHidden** attribute to skip validation on hidden inputs.
-   **[Enable barcode scanning with an external scanner](https://www.servicenow.com/docs/access?context=enable-external-barcode-scanner&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Configure barcode scanning with an external scanner without denying access to the camera for the entire mobile app.

-   **[Mobile Publishing enhancements and changes](https://www.servicenow.com/docs/access?context=mobile-publishing&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**
    -   Enabled Android deep links for multiple instances.
    -   Enhanced validation for transparent images used in branded apps.
    -   Support for public-facing screens in branded mobile apps. Admins can configure URLs that link to public-facing web pages. These web pages are displayed to end users without needing to log in to the mobile app.
-   **[Turn off Zero Trust Access banners in mobile app screens](https://www.servicenow.com/docs/access?context=turn-off-zta-banner&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    In mobile client versions 19.4 and later, you can turn off Zero Trust Access banners on mobile screens. Turning off these banners can enhance usability of your mobile apps because the banner does not display each time the connection state changes so end users are not interrupted by the banner display. You can configure this behavior by setting the **disableZTABanner** mobile property on your ServiceNow instance.


## Activation information

ServiceNow mobile Mobile Platform is a ServiceNow AI Platform® feature that is active by default.

## Accessibility information

The following accessibility updates are available in Mobile Card Builder:

-   Updated alternative text on key images to better support users who rely on screen readers.
-   Enhanced the focus indicator on the Mobile Card Builder home page to improve navigation for users relying on keyboards or Assistive Technology \(AT\).
-   Improved accessible names to provide clear and descriptive labels for interactive elements to support screen readers and other AT.

**Parent Topic:**[Features and changes by product](../new-features-changes.md)

