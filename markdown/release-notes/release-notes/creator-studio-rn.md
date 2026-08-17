---
title: Creator Studio release notes
description: The ServiceNow Creator Studio product is a guided application development experience that enables business process experts to create request-based applications without the barriers of traditional low-code development. Creator Studio was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
---

# Creator Studio release notes

The ServiceNow® Creator Studio product is a guided application development experience that enables business process experts to create request-based applications without the barriers of traditional low-code development. Creator Studio was enhanced and updated in the Yokohama release.

## Creator Studio highlights for the Yokohama release

-   Create forms quickly by using Now Assist.
-   As of Creator Studio version 27.2.2, revamped navigation means you can more easily see what's in your app.
-   Populate any question on the form based on the answer given for a record choice question.
-   Use answers to form questions to trigger an activity in playbooks.
-   Switch seamlessly between no-code, mid-skill, and pro-code app development experiences for a more unified development platform with the new experience switcher.

See  for more information.

**Important:** Creator Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **Generate a form from text prompts using the Build with Now Assist tab**

    Enable users to generate forms automatically from text prompts by using the Build with Now Assist dialog box.

-   **Auto-populate question values on a form**

    Help users complete forms faster with the new **Add auto-fill** option, which automatically populates answers based on answers to questions that are record choices.

-   **Use catalog variables in playbook activities and decisions**

    Playbook activities and decision branches can now be triggered by answers to one or more questions on a form when you configure the conditions.

-   **Select your development experience**

    Seamlessly change between development environments using the new experience switcher. Depending on the products and versions that are installed and the role you have, you can switch between the following environments:

    -   Creator Studio to get a no-code experience
    -   ServiceNow Studio to get a platform coding experience
    -   ServiceNow IDE to get a pro-code ServiceNow experience
-   **Test forms with the new Try it button**

    As of Creator Studio version 27.2.2,you can test using published forms through a **Try it** button. After you submit the form, any associated playbooks run and their results appear in the generated record that opens in a new tab within Creator Studio.

-   **Change the table for an app**

    As of Creator Studio version 27.2.2, admins can change the table where data from apps built in Creator Studio is saved.

-   **Seamlessly open apps in ServiceNow Studio**

    As of Creator Studio version 27.2.2, you can open an app in ServiceNow Studio to make additional, more complicated edits by selecting an **Open with ServiceNow Studio** link from the app's tile on the Creator Studio home page.


## UI changes

-   **Navigation moved from header to sidebar**

    As of Creator Studio version 27.2.2, the navigation has moved from the application header to a navigation panel so you can more easily see what's in your application. The following changes have been made:

    -   The **Forms in your app** section of the navigation panel enables you to easily access forms. If an app has multiple forms, each of them appears separately in the navigation panel.
    -   Automations appear in the navigation panel under the form they're associated with. The link to **Add automation** now appears under each form.
    -   The form submissions section has been renamed **List configurations** and now appears in the **Manage your submission configurations** section of the navigation panel.
    -   The submitted record configuration is now available in the **Record details** in the **Manage your submission configurations** section of the navigation panel.
    -   A search box in the new navigation panel enables you to search all forms and automations in an app.
    -   A bookmark icon \(\[Omitted image "crs-bookmark-icon.png"\] Alt text: bookmark icon\) in the navigation panel enables you to bookmark an app for faster access.
-   **Streamlined app creation**

    As of Creator Studio version 27.2.2, the following changes have been made when you create an app:

    -   A new page appears asking you what type of app you want to build, such as a Service Desk app. Note that admins can choose not to display this page.
    -   Choosing a template, adding a form, and previewing it is now a separate process rather than being done during the app creation process.
-   **Form preview change**

    As of Creator Studio version 27.2.2, the way you preview forms has changed in the following ways:

    -   The option to select between **Portal**, **Now Mobile**, and **Virtual Agent** experiences has moved to the top of the preview.
    -   You can preview only the form you're currently viewing rather than being able to switch between forms in the preview.
    -   The preview no longer shows the record details and workspace configuration. Those items have moved to the new navigation panel.
-   **Request App Workspace more intuitive to use**

    As of Creator Studio version 27.2.2, the Request App Workspace has been streamlined to help fulfillers find and analyze requests more easily. The following changes have been made:

    -   The **Home** view has been removed, so the **Lists** view now appears by default.
    -   The **Analytics** view has been renamed **Dashboard overview**, and the analytics **Home**, **Data Visualizations**, and **KPIs** tabs have been removed.
    -   A link to the **Request App Workspace** now appears in **All** &gt; **App Engine** &gt; **Workspaces**.
-   **Search for apps on the home page**

    Quickly find the app that you're looking for using the new search bar on the Creator Studio home page.

-   **Save and quickly find apps with bookmarks**

    Bookmark apps to find them faster using the new **Bookmarks** pill on the home page.


## Changed in this release

-   **Playbooks use only published forms**

    As of Creator Studio version 27.2.2, forms must now be published \(marked as ready\) before you can use them to create an automated playbook.

-   **Hide the App Engine Studio template with a new system property**

    As of Creator Studio version 27.2.2, Creator Studio users who have both App Engine Studio \(AES\) and Creator Studio installed will no longer see the AES template when they create an app. Admins can choose to show the AES template using the new **com.glide.creator\_studio.template\_deny\_list** system property.

-   **Form location removed from form creation**

    Defining the catalogs and topics for a form is now accomplished by modifying the form settings rather than being done during the form creation process. If you haven't defined a location for a form, you are prompted to do so before you can mark it as ready.


## Activation information

Install Creator Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Additional requirements

You must have the App Engine Enterprise license to use Creator Studio.

## Related ServiceNow applications and features

-   **App Engine Management Center**

    Track and manage your Creator Studio requests, deployments, applications, and collaborative developers using App Engine Management Center.

-   **App Engine Studio**

    Open Creator Studio apps in AES to add more complexity to the app, such as email notifications and additional security.

-   ****

    Create or edit a catalog item using a visual and guided experience.

-   **Form Builder**

    Visually create, configure, and customize the different form views for your users using the form editor in Form Builder.

-   **ServiceNow Studio**

    ServiceNow Studio provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and create custom apps with ease.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio.md)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience.

-   **Workspace**

    Address customer requests and issues in a workspace, which provides a suite of tools where agents, case managers, help desk professionals, and managers work with tools to resolve customer needs.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/build-automate-rn-landing.md)

