---
title: Mobile Platform release notes
description: The ServiceNow Mobile Platform application enables you to access your ServiceNow instance from anywhere. Mobile Platform was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# Mobile Platform release notes

The ServiceNow® Mobile Platform application enables you to access your ServiceNow instance from anywhere. Mobile Platform was enhanced and updated in the Zurich release.

## Mobile Platform highlights for the Zurich release

-   Access Mobile App Builder and Mobile Card Builder inside ServiceNow Studio.
-   Use enhanced capabilities within the input form screen.
-   Engage with the improved error handling when working with uploads.
-   Add customized client-side translations to extend language support on your mobile device.

See [Mobile Platform](https://www.servicenow.com/docs/access?context=mobile-config-navigation&version=zurich&pubname=zurich-mobile&ft:locale=en-US) for more information.

## New in the Zurich release

-   **[Client-side localization](https://www.servicenow.com/docs/access?context=localization-client&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Use the Mobile Custom Localization app, available from mobile client version 20.6, to let mobile users view app content in any language. This feature improves platform consistency and accessibility for global users. The ServiceNow Store app provides a collection of mobile strings that automatically populates the instance with translatable content required for localization. Once these strings are translated into a custom language, the mobile app automatically retrieves and displays them within the app interface.


-   **[Improved error handing for uploads manager](https://www.servicenow.com/docs/access?context=mobile-activity-stream-task&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Use the improved error handling in the upload manager to confirm that the necessary files are uploaded successfully. This feature is available in all areas of the ServiceNow mobile applications where you can upload attachments. This includes the following:

    -   Activity stream
    -   Input form screen with an attachment input type
    -   Input form screen with an attachment input action
    -   Functions of type attachment
    -   Cabrillo JS events within a web page
-   **[Option to save videos and photos locally when using ServiceNow mobile apps](https://www.servicenow.com/docs/access?context=media-saving-mobile-apps&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Enable users to save and retrieve pictures and videos taken with the camera on their ServiceNow mobile app, directly to their device. By default, these images are saved for 24 hours on the phone’s local storage. You can set the storage time to be from 1 to 168 hours \(1 week\).

-   **[Additional descriptive element of type card for input form screens](https://www.servicenow.com/docs/access?context=descriptive-elements-script&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Add cards created in the Mobile Card Builder as a descriptive element in input form screens. Descriptive elements offer more context to users, making it clearer as to what is required for certain inputs within an input form screen.

-   **[Page menu button added to input form screen](https://www.servicenow.com/docs/access?context=parameter-input-screen&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Display a page menu button for input form screens with more than two pages, showing users the current page that they are on, such as "Page 3 of 5." Tapping the button opens a page menu that lists all available pages and their level of completeness. This list helps users track their progress in completing an input form.

-   **[Complete an input form screen in a non-sequential order](https://www.servicenow.com/docs/access?context=parameter-input-screen&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Work on all pages of an input form screen, even if required fields are not completed. Users can use the next and previous buttons at all times, enabling them to complete the form in a non-sequential manner. In addition, users can use the page menu to work on any page of their choosing.

-   **[Error indicator for failed submissions in input form screen](https://www.servicenow.com/docs/access?context=parameter-input-screen&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    View an information icon in the top menu bar in cases where a submitted input form contains at least one error. The icon remains accessible when working through all input form screen pages. Tapping the icon opens a page that lists the validation errors, enabling users to correct these errors and submit an error-free input form.

-   **[Slider option for adding numeric values in input form screen](https://www.servicenow.com/docs/access?context=parameter-screen-var-attr&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Configure sliders as an additional method for users to add numeric values in an input form screen. Sliders offer the advantage of defining minimum, maximum, incremental, and default values.

-   **[New icons added that you can use in your mobile apps](https://www.servicenow.com/docs/access?context=mobile-icon-reference&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Use new icons that have been added to the following font families in your mobile apps:

    -   Actions font icons
    -   Screen font icons
    -   Mobile card font icons
    -   Image icons
-   **[Mobile App Builder and Mobile Card Builder Studio integration](https://www.servicenow.com/docs/access?context=mab-studio-integration&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Develop and modify mobile applications and cards in ServiceNow Studio. Utilize all your necessary tools within a single, cohesive development environment.

-   **[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-mobile-va&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    The following features have been added to ServiceNow Now Assist in Virtual Agent:

    -   Upload documents and files with Doc QnA to have Now Assist generate summaries or answer questions about them.
    -   Search the internet from within Virtual Agent using web search mode.
    -   Capture and analyze data from a variety of visual sources such as images, emails, handwritten notes, websites, and applications using ServiceNow AI Lens.
    -   View shared files when using people citations.
-   **[Now Assist Skill Kit integration](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-for-mobile&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Create and use custom Now Assist skills in your mobile app using Now Assist Skill Kit.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Dark theme support for Mobile App Builder and Mobile Card Builder](https://www.servicenow.com/docs/access?context=mcb-dark-mode&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Added theme selection to Mobile App Builder and Mobile Card Builder that enables you to switch between light and dark mode.

-   **[Mobile App Builder Live component previews](https://www.servicenow.com/docs/access?context=mab-record-example-panel&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Added support for live component previews to the following:

    -   Legacy cards
    -   Analytics previews and chart screens
    -   Launcher screens
    -   Mobile web screens
-   **[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-mobile-va&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    The following UI changes have been made to Now Assist in Virtual Agent:

    -   Follow Now Assist workflow as your request is fulfilled in real-time with chat streaming responses.
    -   Abort the agentic workflow in Virtual Agent before it finishes processing using the **Stop** button.
    -   Open enhanced chat from synthesized responses on the search results page.
    -   Access even more types of citations within Virtual Agent responses such as tables, incidents, PDFs, and third-party connections such as Microsoft SharePoint and Google Drive.
-   **[Attachments in standard search results](https://www.servicenow.com/docs/access?context=sg-mobile-search&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    View attachments such as PDFs, as well as external content from third-party integrations, as a part of your standard search results.

-   **NextGen Search Results**

    Refine search results and quickly find the most relevant information with additional search result filters.

-   **Voice-to-text**

    Enable voice-to-text in search and Now Assist in Virtual Agent by tapping the microphone icon.

-   **Prominent Action Button**

    Access Now Assist or other global functions directly from your tab bar to quickly access it from any screen.

-   **Richer people citations in Now Assist VA**

    View a person’s information in your company’s org chart when searching for an employee in Now Assist in Virtual Agent.

-   **ServiceNow Lens**

    Auto-fill mobile input forms and questionnaires with ServiceNow AI Lens instead of manually entering data.

-   **Doc QnA**

    The following UI changes have been made to Doc QnA.

    -   Upload multiple files simultaneously.
    -   Preview files and attachments before sending them.
    -   Upload multiple files alongside text within a single turn in Virtual Agent.

## Changed in this release

-   **[Enhanced native features in hybrid web screens](https://www.servicenow.com/docs/access?context=url-screen&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Enhanced native features in hybrid web screens that support functionality such as native search, quick actions, and customizable welcome messages within hybrid screen launcher or header tabs.

-   **[Enhanced chat push notifications](https://www.servicenow.com/docs/access?context=using-enhanced-chat-mobile&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Tap enhanced chat push notifications to go directly to the associated chat.

-   **Promoted actions and suggested topics**

    See how Virtual Agent can assist you with suggested actions and topics related to your request.


## Activation information

Mobile Platform is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Features and changes by product](../new-features-changes.md)

